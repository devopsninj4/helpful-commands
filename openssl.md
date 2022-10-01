# OPENSSL

<details><summary>Links</summary>
<p>



</p>
</details>  
  

## Sessions

<details><summary>Generate a pair of keys</summary>
<p>
  
```bash
#Private key
openssl genrsa -out my-key.pem 4096
```
  

```bash
#Public key
openssl rsa -in my-key.pem -pubout my-pub-key.pem
```
</p>
</details>
