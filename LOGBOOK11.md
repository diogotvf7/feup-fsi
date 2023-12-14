# Semana 11

## Becoming a certificate authority

A certificate authority is an entity that issues digital certificates. A digital certificate certifies the ownership of a public key by the named subject of the certificate. This allows others (relying parties) to rely upon signatures or on assertions made about the private key that corresponds to the certified public key.

### Tarefa 1

Command:

```bash
openssl req -x509 -newkey rsa:4096 -sha256 -days 3650 -keyout ca.key -out ca.crt
```

<details>
    <summary>Generated key</summary>
    <hr>

```bash
-----BEGIN ENCRYPTED PRIVATE KEY-----
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
kME1ScPlE9S1MuO4InOkAg==
-----END ENCRYPTED PRIVATE KEY-----
```

</details>

<details>
    <summary>What part of the certificate indicates this is a CA’s certificate?</summary>
    <img src="images/logbook11/root-certificate.png">
</details>

<details>
    <summary>What part of the certificate indicates this is a self-signed certificate?</summary>
    <img src="images/logbook11/self-assigned.png">
</details>

<details>
    <summary>Modulus (n) </summary>
    <img src="images/logbook11/modulus.png">
</details>
<details>
    <summary>Public Exponent (e)</summary>
    <img src="images/logbook11/exponent.png">
</details>

<details>
    <summary>Private Exponent (d)</summary>
    <img src="images/logbook11/private-exponent.png">
</details>

<details>
    <summary>Prime Numbers (p & q)</summary>
    <img src="images/logbook11/prime-numbers.png">
</details>

### Tarefa 2

Gerámos um certificado para o site www.dsg.com através do seguinte comando:

```bash
openssl req -newkey rsa:2048 -sha256 -keyout server.key -out server.csr -subj "/CN=www.dsg2023.com/O=Dsg2023 Inc./C=US" -passout pass:dees
```

Através dos seguintes comando conseguimos ver o conteúdo do CSR e da chave privada:

```bash
openssl req -in server.csr -text -noout
openssl rsa -in server.key -text -noout
```

<details>
    <summary>CSR</summary>
    <img src="images/logbook11/t2-csr.png">
</details>

<details>
    <summary>Private Key</summary>
    <hr>

```bash
RSA Private-Key: (2048 bit, 2 primes)
modulus:
    00:b2:cc:30:fa:58:32:7f:2c:4b:7e:4a:c8:6b:f0:
    1f:97:95:ea:28:50:24:d5:1a:0b:6f:0f:f6:05:b2:
    42:ac:1e:1b:21:5c:c9:7c:6f:83:9a:51:0c:94:e8:
    56:32:a2:ea:be:ad:9e:4f:8a:6a:49:49:4c:75:ff:
    d2:62:fd:af:97:46:3e:b1:f4:7e:70:ec:66:4b:e4:
    aa:47:ef:d5:f8:8b:9e:15:60:73:89:0a:22:40:2f:
    40:d9:ac:ef:bd:1b:71:c6:4a:68:e1:2f:71:49:ca:
    b4:2b:89:31:60:be:95:d8:be:dd:68:37:a2:78:ce:
    07:0e:9a:aa:be:16:50:d0:96:6a:e8:8e:cf:eb:62:
    15:74:6e:6c:b4:4a:d4:e1:ae:a0:4d:67:ab:a7:86:
    ba:09:cc:75:96:e1:26:11:eb:16:bf:2b:c8:2a:13:
    90:05:b5:86:7f:ca:df:54:12:43:d3:6c:d7:db:63:
    c9:05:16:cf:15:fa:b3:f1:3c:30:f3:6b:a8:8a:21:
    95:92:98:be:3f:2e:59:8a:c0:cb:d7:59:96:7c:c6:
    54:89:6e:84:1d:6f:97:e1:e9:ac:52:0d:77:3c:be:
    d2:39:d7:5b:87:27:88:a8:bd:b1:76:5c:6c:17:33:
    8b:20:b4:b3:e4:2a:4b:d5:b2:13:83:84:39:8d:9c:
    ec:ff
publicExponent: 65537 (0x10001)
privateExponent:
    4e:cd:ca:84:7c:5c:fd:4a:33:97:dd:34:0a:c6:d1:
    d5:c8:e0:64:96:36:35:aa:7e:01:9c:62:4d:ce:6c:
    ae:59:b2:91:78:c8:e1:4c:71:0f:91:cb:5e:d2:2c:
    33:b3:34:8d:88:0e:2f:76:8d:33:f1:d7:7e:66:9b:
    7e:bf:db:25:6c:73:73:91:94:2d:07:34:6b:1c:c4:
    a4:62:23:c7:a1:19:b2:c8:49:03:cc:70:9e:23:75:
    8c:bb:39:0a:fb:4e:a1:1b:e8:af:df:6e:2a:1c:ea:
    5e:09:e0:b6:88:29:99:57:3e:54:91:b8:cd:4f:d9:
    32:69:9e:f9:9a:f2:51:8c:4d:c8:02:7c:01:03:1e:
    28:52:78:b9:ab:af:85:dc:d7:7a:ab:f9:44:03:7a:
    5e:7f:c6:a6:9b:eb:a1:b0:84:c0:08:ca:ac:61:f5:
    26:94:94:47:c7:e3:94:63:aa:03:f1:ba:49:51:42:
    6e:ae:77:c0:c1:04:af:db:f6:e3:3d:a0:58:21:f0:
    19:03:fe:ad:a3:87:55:ba:61:88:6d:3c:8f:d6:0a:
    53:95:72:37:d0:d5:9b:44:ff:82:86:41:3d:8b:bf:
    87:e6:38:cd:91:1a:35:03:4e:79:43:b5:3b:21:20:
    ce:f7:b5:6d:34:5d:16:ea:9a:ee:b8:9a:e8:20:b0:
    e1
prime1:
    00:d7:33:4b:3b:e1:c8:25:98:e2:e2:89:5c:a7:62:
    51:c4:d7:3f:cb:66:11:3b:ef:45:fd:1d:35:02:b2:
    de:ea:30:d4:aa:75:fc:cb:90:5d:e1:20:95:c9:ff:
    c0:d7:46:92:44:9f:ca:1f:2b:28:8b:5a:bb:0b:63:
    57:7f:a2:b8:37:1c:85:a8:1b:74:9e:d9:79:84:4d:
    05:b1:63:d1:94:6c:67:fd:fd:d2:97:c5:17:9e:38:
    eb:b6:35:d4:93:62:28:d3:8d:c1:80:31:08:c3:1b:
    f0:69:63:91:1a:be:71:e9:1a:ed:7a:d9:57:b6:dd:
    18:c6:df:ed:1e:e5:23:39:cf
prime2:
    00:d4:b2:18:fe:23:42:02:1e:aa:73:d7:59:e7:0a:
    f4:d5:15:ae:50:b9:4f:db:a8:a7:d6:63:e6:86:11:
    f3:06:ce:03:a3:fb:2e:1f:f6:17:fa:33:e9:52:4d:
    70:3c:74:a4:a2:6e:97:70:ef:73:48:0d:f2:e7:3b:
    8b:3e:4a:fa:dc:d6:76:29:55:64:18:b7:d1:58:38:
    9e:9d:be:d9:4c:11:2d:b4:f2:14:fd:69:92:84:c9:
    4f:1e:8e:1c:43:f8:d1:19:85:42:8b:99:ac:3b:53:
    69:40:9f:a8:27:a8:69:53:3f:f0:92:a5:2f:c7:a0:
    c3:53:e9:95:55:bb:07:55:d1
exponent1:
    1d:df:e7:0f:d7:16:3b:f1:ef:7d:57:68:5f:6c:4c:
    c1:b0:c8:10:6a:88:f5:f3:0f:9a:45:d5:b8:1c:30:
    c9:fe:21:67:d0:9d:59:7d:1f:2b:43:a4:c7:b8:13:
    83:4f:2e:bb:0c:1b:b9:1b:fa:b2:ed:d3:8d:8f:2a:
    f4:73:18:73:be:27:e7:e0:77:de:1d:7e:bb:19:1e:
    33:34:12:42:32:92:75:36:29:68:1c:5a:5d:02:b5:
    e6:43:ae:d1:0f:0d:6f:e0:fb:fd:d9:d0:c7:95:37:
    58:ca:13:b8:cc:bb:6f:8a:e7:70:e8:7f:3e:c9:8e:
    c8:fd:09:24:02:d7:53:0d
exponent2:
    62:b7:5a:34:31:87:04:56:d9:43:b4:92:8c:52:20:
    79:f9:7b:13:0a:3f:0f:33:02:da:d5:38:fb:c6:be:
    e5:cc:9e:11:f0:95:62:ce:24:28:c3:09:2a:62:b8:
    91:c6:8d:56:ba:3f:5d:72:35:2e:1f:13:3a:d0:fe:
    fa:65:70:73:28:b2:64:d2:b6:07:66:e1:29:b1:f5:
    a4:3f:1c:b9:5a:4b:bd:6c:91:e3:5f:a9:5a:29:d8:
    a7:d4:cb:37:9c:f6:e7:82:5a:f5:51:d8:87:1c:5a:
    80:5c:d9:7d:b6:83:53:d9:1c:3d:e3:9e:fe:67:15:
    e1:0f:4b:79:23:b9:ee:d1
coefficient:
    37:47:ac:9b:bc:87:9e:0b:aa:9d:b4:37:0b:f9:c3:
    ab:ca:86:c7:c1:46:c1:2d:8f:9b:fb:5f:5d:61:b6:
    e3:12:e4:d7:6c:76:d3:c0:ce:e6:55:5c:88:f0:07:
    44:59:4a:99:02:6d:a6:e8:bf:37:72:cb:11:7d:e6:
    47:12:f5:29:51:dc:6e:c8:23:82:c0:e5:aa:fc:fb:
    e9:cd:e2:f6:41:e5:03:57:4b:6a:12:54:26:9b:0e:
    a2:ab:bb:71:e1:69:26:f9:8b:0f:f9:0d:4d:35:4d:
    f8:dd:82:b3:4f:60:dc:a6:b4:6a:00:70:73:7e:61:
    10:ad:e2:ca:ce:ce:29:b8
```

</details>

Com o seguinte comando adicionamos 2 nomes alternativos ao certificado:

```bash
openssl req -newkey rsa:2048 -sha256 -keyout server.key -out server.csr -subj "/CN=www.dsg2023.com/O=Dsg2023 Inc./C=US" -passout pass:dees -addext "subjectAltName = DNS:www.dsg2023.com, DNS:www.dsg2023A.com, DNS:www.dsg2023B.com"
```

Ao correr o comando `openssl req -in server.csr -text -noout` podemos verificar que os nomes alternativos foram adicionados:

```bash
Requested Extensions:
            X509v3 Subject Alternative Name: 
                DNS:www.dsg2023.com, DNS:www.dsg2023A.com, DNS:www.dsg2023B.com
    Signature Algorithm: sha256WithRSAEncryption
```

### Tarefa 3

De maneira a tornar válido o CSR criado na tarefa anterior, é necessário assiná-lo com a chave privada da CA. Para isso, usamos o seguinte comando:

```bash
openssl ca -config openssl.cnf -policy policy_anything -md sha256 -days 3650 -in server.csr -out server.crt -batch -cert ca.crt -keyfile ca.key
```

No entanto, antes de podermos correr este comando devemos alterar o ficheiro `openssl.cnf` de modo a que o campo `copy_extensions` esteja descomentado. Por motivos de segurança, este campo está desativado, uma vez que permite que o comando `openssl ca` copie o campo de extensão do pedido para o certificado final.

<details>
    <summary>Output</summary>
    <hr>
    
```bash
$ sudo openssl ca -config openssl.cnf -policy policy_anything -md sha256 -days 3650 -in server.csr -out server.crt -batch -cert ca.crt -keyfile ca.key
Using configuration from openssl.cnf
Enter pass phrase for ca.key:
Check that the request matches the signature
Signature ok
Certificate Details:
        Serial Number: 4096 (0x1000)
        Validity
            Not Before: Dec 11 00:36:31 2023 GMT
            Not After : Dec  8 00:36:31 2033 GMT
        Subject:
            countryName               = US
            organizationName          = Dsg2023 Inc.
            commonName                = www.dsg2023.com
        X509v3 extensions:
            X509v3 Basic Constraints: 
                CA:FALSE
            Netscape Comment: 
                OpenSSL Generated Certificate
            X509v3 Subject Key Identifier: 
                6A:25:CC:5F:66:E7:AC:27:A4:27:D5:0C:C4:C9:BE:25:77:DF:7E:90
            X509v3 Authority Key Identifier: 
                keyid:0C:BC:0B:55:E2:DE:62:AE:BA:26:A4:E6:3F:9F:34:E0:47:07:9D:5B

            X509v3 Subject Alternative Name: 
                DNS:www.dsg2023.com, DNS:www.dsg2023A.com, DNS:www.dsg2023B.com
Certificate is to be certified until Dec  8 00:36:31 2033 GMT (3650 days)

Write out database with 1 new entries
Data Base Updated
```

</details>

<hr>

# Tarefa 4

Nesta tarefa configuraremos um servidor Apache para suportar HTTPS. Para isso, apenas precisamos de configurar o servidor Apache para que ele saiba onde obter a chave privada e os certificados.
Como um servidor Apache pode hospedar vários sites, ele precisa de saber em que pasta estão os ficheiros de cada site. Esta tarefa é feita através do ficheiro VirtualHost, localizado na pasta `/etc/apache2/sites-available`. Na config do nosso container, é feita uma cópia do ficheiro `dsg2023.conf` para a pasta `/etc/apache2/sites-enabled`, que é a pasta onde o Apache procura os ficheiros de configuração dos sites que estão ativos.

```bash
<VirtualHost *:443> 
    DocumentRoot /var/www/dsg2023
    ServerName www.dsg2023.com
    ServerAlias www.dsg2023.com
    ServerAlias www.dsg2023A.com
    ServerAlias www.dsg2023B.com
    ServerAlias www.dsg2023W.com
    DirectoryIndex index.html
    SSLEngine On 
    SSLCertificateFile /certs/dsg2023.crt
    SSLCertificateKeyFile /certs/dsg2023.key
</VirtualHost>

<VirtualHost *:80> 
    DocumentRoot /var/www/dsg2023
    ServerName www.dsg2023.com
    DirectoryIndex index_red.html
</VirtualHost>

# Set the following gloal entry to suppress an annoying warning message
ServerName localhost
```

Ao corrermos o comando:

```bash
service apache2 start
```

o servidor Apache começa a correr e podemos aceder ao site através do browser. No entanto, como o certificado não é assinado por uma CA reconhecida, o browser mostra um aviso de segurança:

![Alt text](images/logbook11/dsg-unsafe.png)

Para resolver este problema, acedemos ao link `about:preferences#privacy` e abrimos o menu `View Certificates`. Neste menu, importamos o certificado da CA que criámos no início da tarefa:

|||
| -- | -- |
| ![Alt text](images/logbook11/add-ca.png) | ![Alt text](images/logbook11/feup-dsg.png) |

Depois de importar o certificado, o browser já não mostra o aviso de segurança:

![Alt text](images/logbook11/dsg-safe.png)

# Tarefa 5

Nesta tarefa, devemos tentar simular um man-in-the-middle attack. Para tal, devemos editar o campo `ServerName`
no nosso ficheiro `dsg2023_apache_ssl.conf` para ter o link para o site que pretendemos simular. Neste caso, vamos simular o site do Facebook. Deixamos os restantes campos iguais. Depois devemos também editar o ficheiro `/etc/hosts` adicionando a linha: `10.9.0.80 www.facebook.com` para que, quando o browser tentar aceder ao site do Facebook, seja redirecionado para o nosso servidor Apache.

Depois de correr o comando `service apache2 start`, podemos aceder ao site do Facebook através do browser. No entanto, como o certificado não é assinado por uma CA reconhecida, o browser mostra outra vez um aviso de segurança:

![Alt text](images/logbook11/facebook-unsafe.png)

Isto acontece porque o certificado que estamos a usar apenas assinou o site www.dsg2023.com e não o site www.facebook.com. Este promenor é verificado pelo browser e, como o certificado não é válido para o site que estamos a tentar aceder, o browser mostra o aviso de segurança.

# Tarefa 6

De modo a completar o nosso man-in-the-middle attack, devemos adicionar um certificado para a nossa versão atualizada do site www.dsg2023.com, agora com o nome www.facebook.com. Para isso corremos o comando:

```bash
$ openssl req -newkey rsa:2048 -sha256 -keyout server.key -out server.csr -subj "/CN=www.facebook.com/O=Dsg2023 Inc./C=US" -passout pass:dees -addext "subjectAltName = DNS:www.facebook.com, DNS:www.dsg2023.com, DNS:www.dsg2023A.com, DNS:www.dsg2023B.com"
```

de modo a criar um pedido de certificação para o nosso site mascarado. Podemos aceitá-lo com a nossa self-signed key através do comando:

```bash
openssl ca -config openssl.cnf -policy policy_anything -md sha256 -days 3650 -in server.csr -out server.crt -batch -cert ca.crt -keyfile ca.key
```

Deste modo, o nosso site já é coniderado seguro pelo browser. Se acedermos ao mesmo através do firefox obtemos o seguinte resultado:

![Alt text](images/logbook11/facebook-safe.png)

