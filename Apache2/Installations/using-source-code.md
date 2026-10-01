# Installation Apache Using Source Code
## What is "source code"?
Source code is software written mainly in programming languages such as C.
The source code is the human-readable code used to build packages like Apache.
### Why?
Because when installing from source, you are starting with the original Apache code, rather than a pre-built Ubuntu package.
## Step 1:
### Install Dependencies
These are tools and libraries required to build Apache.
### For example:
- gcc → compiler
- make → builds the software
- development libraries → provide functionality Apache needs
### command
```
sudo apt update

sudo apt install -y build-essential \
libpcre2-dev \
libapr1-dev \
libaprutil1-dev \
libssl-dev \

```

<img width="1315" height="654" alt="image" src="https://github.com/user-attachments/assets/466a7c6f-5dab-4a49-b584-5a6ec256a268" />

### Why?
Your Linux machine doesn't automatically have everything required to compile Apache.
## Step 2
### Download Apache Source Code
```
 wget https://dlcdn.apache.org/httpd/httpd-2.4.68.tar.bz2
```

<img width="1306" height="495" alt="image" src="https://github.com/user-attachments/assets/22c009ba-bc2f-4e5d-9358-7c6cb59e2133" /> 

###  What?

-  ``wget`` downloads the Apache source-code archive.
-  ``.tar.gz`` is a compressed archive containing the source code.

### Why?
We need to get the Apache source code onto our Linux server before we can build it.

## Step 3:
Extract the Source Code
```
tar -xf httpd-2.4.68.tar.bz2 httpd-2.4.68/

```
### What?
This extracts the compressed archive.

### Why?
You cannot normally compile the source while it is still inside the compressed archive. You need the actual files.
<img width="1276" height="117" alt="image" src="https://github.com/user-attachments/assets/7302f1ab-1936-42a8-b4c4-e0dac9fe642b" />
## Step 4:
### Create directory 
```
mkdir httpd
```
### What 
Make directory where we can install our apache

<img width="1276" height="117" alt="image" src="https://github.com/user-attachments/assets/8b3ecca8-f645-4342-8a41-cc41bc971b30" />
### Why 
Here the all apache file are availble

## Step 5:
### Enter the Apache Directory

```
 cd httpd-2.4.68/
```
### What?
Moves you into the Apache source-code directory.
<img width="1303" height="139" alt="image" src="https://github.com/user-attachments/assets/65ee4748-1329-43c4-8239-901f4da0e3fa" />

### Why?
The Apache build commands such as ./configure and make need to be executed from the source directory.
## Step 6:
### Configure Apache
```
./configure --prefix=/home/ubuntu/http
```
This is a very important step.

- What does ./configure do?

- It checks your system and prepares Apache for compilation.

- It determines things such as:

- Which libraries are available
- Which compiler can be used
- Which features can be enabled
- Where Apache should be installed

- --prefix tells Apache:

- "Install Apache under this directory."


### Why?
The source code needs to be configured for your particular Linux system before compilation.
## Step 7:
### Compile Apache && Install Apache
```
make && make install
```
### What?
``make`` uses the compiler to convert the Apache source code into machine-executable programs.
This copies the compiled Apache files into the location specified during configure.
<img width="1308" height="523" alt="image" src="https://github.com/user-attachments/assets/7ae04683-8658-475e-bd1e-ea800ac6402c" />

### Why?
Your computer cannot directly run the Apache C source code.
It needs to be compiled into executable code.
- ``make`` builds Apache.
- ``make install`` puts the built Apache files in their final location.
## Step 8:
### Start Apache
```
/home/ubuntu/httpd/bin/apachectl start
```
### What?
Starts the Apache web server.
<img width="1303" height="79" alt="image" src="https://github.com/user-attachments/assets/d73e65c5-d5a5-4b54-83f5-68a780ea5846" />
### Why?
Installing Apache doesn't necessarily mean that Apache is currently running.
You need to start the web server so it can listen for client requests.
### Step 9
Test Apache
```
curl http://localhost
```


### What?
curl sends an HTTP request to Apache.
<img width="1312" height="399" alt="image" src="https://github.com/user-attachments/assets/801f7a2e-8037-4032-8669-c9d49395b2b2" />
### Why?
We want to verify that Apache is actually running and responding to requests.
If Apache is working, you should receive HTML content.
