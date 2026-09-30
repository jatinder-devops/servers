# ``httpd`` (apache2) Installation in amazone-Linux
In amazone linux  apache2 is known as httpd. This is the installation guide for installing httpd in amazon linux.
## Step for installing httpd.
## Step 1:
First you have to check the package is available or not.
```
httpd --version
```
<img width="1485" height="72" alt="image" src="https://github.com/user-attachments/assets/3c75c0df-8e2e-46c2-9c93-16c60f46c22a" />

### Step 2: 
Now enter the command for inatalling
```
sudo dnf install httpd
```

<img width="1488" height="500" alt="image" src="https://github.com/user-attachments/assets/fee3b884-90be-4d6a-9852-dfbf346af937" />

### Step 3:
verify
```
which httpd
```
<img width="1477" height="114" alt="image" src="https://github.com/user-attachments/assets/505352fe-4b2a-4694-8440-69ae96e73e5c" />

### Step 4: 
Check status
```
sudo systemctl status httpd
```
<img width="1455" height="181" alt="image" src="https://github.com/user-attachments/assets/76506256-c121-44d3-9d51-869655317dbc" />

### Step 5: 
Start server httpd
```
 sudo systemctl start httpd
```
<img width="1461" height="810" alt="image" src="https://github.com/user-attachments/assets/90afb9da-4740-4500-af4b-7043f1884e97" />

### Step 6:
Enable server 
```
sudo systemctl enable httpd
```
``Enable`` means while the machine restart the service will be automatically start.
``Disable`` means when the machine is restart the service will remain stop. 
<img width="1470" height="663" alt="image" src="https://github.com/user-attachments/assets/1a8fc506-f10b-45a8-8163-657523e6e640" />
