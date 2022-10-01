# OPENSSL

<details><summary>Links</summary>
<p>
https://wiki.openssl.org/index.php/Command_Line_Utilities


</p>
</details>  
  

## Keys generation

<details><summary>Generate a pair of keys</summary>
<p>
  
```bash
#Private key
openssl genrsa -out my-key.pem 4096
```
  
```bash
#Private key - method 2
openssl genpkey -algorithm RSA -pkeyopt rsa_keygen_bits:4096 -out my-key.pem
```
  
```bash
#Public key
openssl rsa -in my-key.pem -pubout my-pub-key.pem
```
</p>
</details>
