1. Install [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
2. In the Windows start menu, search for and run puttygen.exe

 ![image](https://user-images.githubusercontent.com/219478/180890260-c862d9e2-c67e-4698-bc2e-6967ce7ab63f.png)
 
    a. Select EdDSA <br>
    b. Click Generate <br>
    c. Set your email in the Key Comment field <br>
    d. Copy public key <br>
    
3. Run the following commands

CMD:
```cmd
mkdir -p %userprofile%\.ssh
notepad %userprofile%\.ssh\id_ed25519.pub
  ```
Powershell:
```powershell
mkdir -p $home\.ssh
notepad $home\.ssh\id_ed25519.pub
```
4. Paste your public key into notepad, save the file and exit
5. Optional: set a passphrase in the Key passphrase field

![image](https://user-images.githubusercontent.com/219478/180891520-9020abfe-c89d-46aa-aea0-7a5fb36c93a7.png)

6. Choose Export OpenSSH key from the Conversions menu and save the file to ~/.ssh/id_ed25519
7. Click Yes to save the file without a passphrase 
8. paste %userprofile%\.ssh\id_ed25519 into the File name: field of the save file dialog box and click Save
9. Click the Save private key button
10. Click Yes to save the file without a passphrase 
11. paste %userprofile%\.ssh\id_ed25519.ppk into the File name: field of the save file dialog box and click Save
12. exit puttygen
