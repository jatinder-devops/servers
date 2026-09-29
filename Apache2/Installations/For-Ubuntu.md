# Apache2 Installation on Ubuntu
Apache2 is a service which help us to hosting websites
## Step for installation:
### Step 1:
First check apache2 in available on our machine or not:
### Command:
```
apache2 --version
```
<img width="1591" height="217" alt="image" src="https://github.com/user-attachments/assets/c1bb090c-8f69-4704-98c0-b0e5b3c486c0" />

### Step 2:
Then you have to update your system packages for getting latest version of your packages.
```
sudo apt update
```
<img width="1668" height="768" alt="image" src="https://github.com/user-attachments/assets/bdd7ebe5-53eb-43fe-8779-6ec3f6332c52" />

### Step 3:
Enter the command for installation:
### Command:
```
sudo apt install apache2
```
<img width="1303" height="553" alt="image" src="https://github.com/user-attachments/assets/4ac2ac2c-d271-43f7-8280-6a11343182f3" />

### step 4:
Verify, whether the apache2 is installed and running.
### Command:
```
sudo systemctl status apache2
```
<img width="1675" height="604" alt="image" src="https://github.com/user-attachments/assets/77cdd783-2629-42a7-91a3-42805d2b3570" />
