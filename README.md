# Working With SSH In Ubuntu
This is a brief tutorial of how to get started using SSH with Ubuntu. 
I have included screenshots of the examples to help you follow along. 
While your terminal may be identical to mine, the commands and methods are still the same.

We will cover:
- installing OpenSSH
- Checking the status of OpenSSH
- Stopping/starting SSH
- Enabling/disabling OpenSSH

## To check if SSH is already installed, we can use:

[ systemctl status ssh ] 

![ssh_active](https://user-images.githubusercontent.com/55526410/120088238-a33cfd80-c0bc-11eb-987c-c7475833ec72.png)

If we receive any errors like below that the service can not be found, we can continue with installing OpenSSH

![ssh1](https://user-images.githubusercontent.com/55526410/120088106-98ce3400-c0bb-11eb-9d68-ab18fdfb64a1.png)


## Install OpenSSH using the following command:

OpenSSH should come with Ubuntu by default. If your system does not include a copy, you can easily install it:

[ sudo apt install openssh-server ]

## Stopping/Starting SSH

To start or stop SSH, you can use the following command:

[ sudo systemctl start/stop ssh ]

![ssh_inactive](https://user-images.githubusercontent.com/55526410/120088120-a7b4e680-c0bb-11eb-9110-9f39f3b00f6b.png)

## Disbabling the daemon

A daemon is a program that instructs the service to start when the system is booted. You can disable this by using the following command:

[ sudo systemctl disable ssh ]


![ssh_inactive_disabled](https://user-images.githubusercontent.com/55526410/120088121-a7b4e680-c0bb-11eb-8726-6446b709d82d.png)

When we check our output again, we see that SSH is set to disabled which means it will not start on boot. 

## SSH Into Server

To SSH into another server we use the 'ssh' command following by the ip address. You also have the option to set you username as well. I've chosen 'user'

[ ssh example@10.0.0.0 ]

![ssh_into](https://user-images.githubusercontent.com/55526410/120088472-c9639d00-c0be-11eb-809c-7a344ba17dda.png)







