

# WebGoat Assignments lesson 6 - Crypto Basics

1) create file "private.key" from assignment private key.

   

2) get **public key** from **private one** : 

   ```shell
   openssl rsa -in private.key -pubout > key.public
   ```

   

3) get **modulus** key from **public key**

   ```shell
   openssl rsa -in key.public -pubin -modulus -noout > modulus.key
   ```



4. get **sha256 ** key from **modulus**

   ```shell
   echo -n "modulus.key content as test" | openssl dgst -sign t.pub -sha256 -out sign.sha256
   ```
   
   

5) Encode sha256 to base64 :

   ```shell
   openssl enc -base64 -in sign.sha256 -out sign.sha256.base64
   ```
   
   Video tutorial on YouTube : 