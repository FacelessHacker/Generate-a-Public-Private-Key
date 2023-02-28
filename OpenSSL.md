# How to Generate a Public\Private Key & Encrypt\Decrypt Using Both Keys With OpenSSL on Linux

### Generating Public & Private Keys on Linux
##### Step 1
- Make sure openssl is installed on your linux. It comes preinstalled on linux anyways.
- On your terminal, enter this command
- 
  ```
  openssl genrsa -out private-key.pem 1024
  ```
- After using this command, the private key is generated and saved as 'private-key.pem'. You can list the files on the directory you are to check using 'ls' command.
- Now, enter the below command to generate the public key
  ```
  openssl rsa -in private-key.pem -pubout -out public-key.pem
  ```
- You can use the 'ls' command again to check the public key generated. It will be saved as public-key.pem in the directory you are.

##### Encrypting & Decrypting a File/Word
- You can write something in a file, save it, encrypt it and try to decrypt it again using the earlier generated private and public keys.
- For example, echo "hello-world"> plaintext


![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/1.png)
