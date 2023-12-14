# CTF Semana #11 (Public Key Infrastructures)

## Introdução

Para este CTF é-nos dado um ficheiro `challenge.py` que contém o código que corre na porta `6004` do servidor `ctf-fsi.fe.up.pt`. Este código tem 3 funções das quais apenas duas são relevantes para a resolução do desafio: `enc` e `dec`. Estas funções baseiam a sua encriptação no algoritmo RSA, que é um algoritmo de encriptação assimétrica. 
Este algoritmo baseia-se na existência de duas chaves, uma pública e outra privada. Chaves públicas são usadas para encriptar mensagens e chaves privadas são usadas para desencriptar mensagens. 
Ao corrermos o comando `nc ctf-fsi.fe.up.pt 6004` obtemos o seguinte output:

```bash
Public parameters -- 
e:  65537 
n:  359538626972463181545861038157804946723595395788461314546860162315465351611001926265416954644815072042240227759742786715317579537628833244985694861278997871052684504401596494019122799039009989371808178352060966438579515613360227960308969957859170183912581829276320781354104234997246446865042463594219967161283
ciphertext: 6535613362666334393663366231316539643735383937373166613363663463386432386631343636313139343064303637643766396632366532336434666131656331383135623633323239643732326530373833356166306363303138306335383362653331313862353337396338333833393961393336653938636564326464323366623265656330353534366532366265386262366539636634363638623830353338653030653333653765316132346533643364363161363462666563623439343464663665616433333636646639333766333138643335346636363139336534303634353838323932663138373239383863616663306464303230303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030
```

Também nos é dada uma pista que num situação que torna o algoritmo vulnerável. Sabemos que os valores de `p` e `q` são primos próximos de 2⁵¹² e 2⁵¹³, respetivamente. O facto de sabermos estes valores cria a possibilidade de calcularmos a chave privada por brute force.

Foi-nos sugerido também o uso do algoritmo `Miller-Rabin`, um algoritmo probabilístico para a determinação da primalidade de um número. 

## Cálculo da chave privada

Como o valor de `n` é dado e sabemos que:

$$ n = p \times q $$

podemos iterar todos os valores próximos de 2⁵¹² e ver quais os que dividem `n` sem resto e, ao mesmo tempo são primos (é aqui que é usado o algoritmo Miller Rabin). Caso um hipotético valor `p` divida `n` sem resto, podemos calcular o valor de `q`.  

Tendo `p` e `q` podemos, agora, calcular o valor de `d` que é a chave privada.

$$ ed \% (p-1)(q-1) = 1 $$
$$ d = \frac{1}{e} \% (p-1)(q-1) $$

A partir destes valores já podemos desencriptar a mensagem. 

## Resolução

```python
lower_limit = 2**512 - 100000
upper_limit = 2**512 + 100000
for i in range(lower_limit, upper_limit + 1):
    if is_Prime(i):
        if n % i == 0 and is_Prime(n // i):
            q = n // i
            
            d = pow(e, -1, (i-1)*(q-1))
            flag = dec(unhexlify(ciphertext), d, n)
            print(flag.decode())
            break
else:
    print("Failed to find key")
```




