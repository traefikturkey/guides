1. Install [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
2. In the Windows start menu, search for and run puttygen.exe

 ![image](https://user-images.githubusercontent.com/219478/180890260-c862d9e2-c67e-4698-bc2e-6967ce7ab63f.png)
 
    a. Select EdDSA 
    b. Click Generate 
    c. Set your email in the Key Comment field 
    d. Copy public key 
    
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
6. Choose Export OpenSSH key from the Conversions menu 


![image](https://user-images.githubusercontent.com/219478/180891520-9020abfe-c89d-46aa-aea0-7a5fb36c93a7.png)


7. Click Yes to save the file without a passphrase 

![image](https://user-images.githubusercontent.com/219478/180892771-921ca279-e753-4207-933b-d5358af72230.png)

8. paste the following into the File name: field of the save file dialog box and click Save
> %userprofile%\\.ssh\id_ed25519

![image](https://user-images.githubusercontent.com/219478/180893381-41f1d001-7106-4d2d-bdff-aef6ed6024dc.png)

9. Click the Save private key button

![image](https://user-images.githubusercontent.com/219478/180892607-51e8ebf4-7d7e-4948-9612-c0eff057a7fc.png)

10. Click Yes to save the file without a passphrase 

![image](https://user-images.githubusercontent.com/219478/180892771-921ca279-e753-4207-933b-d5358af72230.png)

11. paste the following into the File name: field of the save file dialog box and click Save
> %userprofile%\\.ssh\id_ed25519.ppk

![image](https://user-images.githubusercontent.com/219478/180893388-42f71f04-0be9-4d8f-b8f2-401ab8192d39.png)

12. exit puttygen
