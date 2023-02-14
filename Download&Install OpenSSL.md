# Download, Install & Execute OpenSSL on Windows 11

## Download Openssl File

Click on the link below to download OpenSSL binary Zip file
https://sourceforge.net/projects/openssl/files/
 Download the latest file

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(54).png)


- Open the downloaded zip file and extract to your preferred location
- Click OKay

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(55).png)


- Open your explorer to check the chosen location for the OpenSSL file

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(56).png)


## Setting OpenSSL_Conf file on Windows

- On your file Explorer, right Click on 'This Pc'

- Right Click on Properties

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(57).png)

- Under system about window, click on 'Advanced System Settings'


![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(60).png)

- System Properties box will appear

- Click on Environment Variables


![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(61).png)


- System Properties box will appear with 2 segments: user variables for admin & System Variables


- Choose on 'Path' under 'User variables for admin

- Click on edit


![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screoenshot%20(62).png)


- On the edit environment variable box,

- Choose New

- Enter the full path of the OpenSSL file (C:\OpenSSL\bin)

- Click on Okay

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(63).png)


- Go back to the previous box

- Under System Variables, click on 'New'

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(64).png)

- A box will appear,

- Enter the Variable name (OPENSSL_CONF)

- Enter the Variable Value - that is, the full path of openssl.cnf file
 (C:\OpenSSL\bin\openssl.cnf)
 
 - Click okay
 
![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(65).png)


The Settings is done!

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(66).png)

![UI Image](https://github.com/FacelessHacker/Generate-a-Public-Private-Key/blob/main/Screenshot%20(67).png)

## Execute OpenSSL through the Command Prompt

- Open cmd
- Type the below in the terminal to confirm OpenSSL successful installation

```

openssl version

```

