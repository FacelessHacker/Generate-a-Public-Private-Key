# Generate a Public\Private Key & Encrypt\Decrypt Using Both Keys With OpenSSL on Linux

### Generating Public & Private Keys on Linux

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

   ![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/1.png)


### Encrypting & Decrypting a File/Word
- You can write something in a file, save it, encrypt it and try to decrypt it again using the earlier generated private and public keys.
- For example, we can use this command to write 'hello-world' and save in into a file named as plaintext.
- 
  ```
  echo "hello-world"> plaintext
  ```
 - Use the 'ls' command to check the file just created in the directory you are.
 - The next thing is to encrpt the file created using this command.
 
 ```
 openssl pkeyutl -encrypt -in plaintext -out encryptplaintext -inkey public-key.pem -pubin
 ```
 
 The break down of the command for better understanding is 
 openssl pkeyutl -encrypt -in (name of the file to encrypt) -out (name to save the encrypted file as) -inkey (name of the publickey earlier generated) -pubin
 
 - You can as well use the 'ls' command to see the just created encrypted file. In this write-up, it is saved as 'encryptplaintext' and the 'cat' command as well to view the content. You will see that the content is no longer in plain text.
 
 ![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/2.png)
 
- Use the command below to decrypt the encrpted file back to the original form to be able to read the content of the file.

  ```
  openssl rsa -decrypt -in encryptplaintext -out decryptplaintext -inkey private-key.pem -pubin
  ```
  
   ![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/3.png)
