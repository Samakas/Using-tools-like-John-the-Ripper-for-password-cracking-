# Using-tools-like-John-the-Ripper-for-password-cracking

### Name: Samakash R S
### Reg NO: 212223230182

## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).

### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:

- **Install the John Ripper**
  ```bash
  sudo apt install john
  ```
- **Create a Password-Protected ZIP File**
   Archive a normal file (secret.txt) into a password-protected ZIP file
   ```bash
   zip --password 123abc secret.txt.zip secret.txt
   ```
 - **Extract the Hash from the ZIP File**
   ```bash
   zip2john secret.txt.zip > zip_hash.txt
   ```
- **Crack the ZIP Password using John**
  ```bash
  john --format=zip zip_hash.txt
  ```
- **Show the Cracked Password**
  ```bash
  john --show zip_hash.txt
  ```

## OUTPUT:
### Create a Password-Protected ZIP File
![lab7(1)](https://github.com/user-attachments/assets/2ec5bb51-6fd8-41a3-be3a-c21177609105)


### Extract the Hash from the ZIP File
![lab7(2)](https://github.com/user-attachments/assets/25a49c2e-1e4e-44fc-8427-2f7ffc57dd9e)


![lab7(5)](https://github.com/user-attachments/assets/271cda33-40a6-49b7-b690-a0c23cdad607)


### Crack the ZIP Password using John
![lab7(3)](https://github.com/user-attachments/assets/e2e3bac8-7bff-4b61-94ac-86686e59f514)


### Show the Cracked Password
![lab(4)](https://github.com/user-attachments/assets/71be194d-68be-4245-83c9-7d73de01f311)


## RESULT:
The password hashes were successfully cracked using John the Ripper.

