## Part 1. Installation of the OS

  `cat /etc/issue` 


![OS verison](images/part1.1.png "OS version")
  |:--:| 
| *OS version* |


## Part 2. Creating a user

![User_creation](images/part2.1.png)
  |:--:| 
| *Command to create a 'test_user' user and add him to adm group* |



`cat /etc/passwd`


![checking_user](images/part2.2.png)
  |:--:| 
| *now user 'test_user' is in adm group* |


## Part 3. Setting up the OS network

1. 
![Changing machine name](images/part3.1.png)
  |:--:| 
| *Сhanging machine name to 'user-1'* |


2. 
![Setting time zone](images/part3.2.png)
  |:--:| 
| *Setting time zone* |


3. 
![Checking network interfaces](images/part3.3.png)
  |:--:| 
| *Checking network interfaces* |

>lo is the loopback interface. \
>This is a special network interface that the system uses to communicate with itself. It is a set of methods necessary to correct the router's operation and data transmission. \
>The interface is needed to display processes in the router.

4. 
![Getting current DHCP server ip-address](images/part3.4.png)
  |:--:| 
| *Getting current DHCP server ip-address* |

>DHCP (Dynamic Host Configuration Protocol) is a protocol that automatically configuring device's IP adresses. \
>It takes 4 steps to configure IP to client, this process named DORA: \
>D: Discover \
>O: Offer \
>R: Request \
>A: Acknowledgement

5. 
![Getting internal and external ip-addresses](images/part3.5.png)
  |:--:| 
| *Getting internal and external ip-addresses* |

6. 
![static](images/part3.6.1.png)
  |:--:|
![static.2](images/part3.6.2.png)
![static.3](images/part3.6.3.png)
| *Setting static ip address* |

7. 
![checkip](images/part3.7.1.png)
  |:--:|
![checkip.2](images/part3.7.2.png)
| *Checking changes* |



## Part 4. OS Update
![update](images/part4.1.png)
  |:--:|
| *Updating OS* |



## Part 5. Using the sudo command

![sudo user](images/part5.1.png)
  |:--:|
| *Giving sudo rights to 'test_user'* |

> The sudo command allows us to run programs with the security privileges of another user (by default, as the superuser).

![sudo](images/part5.2.png)
  |:--:|
| *Changing hostname using 'test_user'* |


## Part 6. Installing and configuring the time service

![time service](images/part6.1.png)
  |:--:|
| *Checking time service* |

## Part 7. Installing and using text editors

1. *==VIM==*

![vim](images/part7.1.1.png)
  |:--:|
![vim.2](images/part7.1.2.png)
![vim.3](images/part7.1.3.png)\
| *Using VIM* |

  >to enter editing mode press 'i' \
  >to exit editing mode press ESC \
  >to save & exit type ':wq' and then press ENTER \
  >to exit without saving changes type ':q' press ENTER \
  >to search /<search text> \
  >to search & replace :s/<search text>/<replacement text>

2. *==NANO==*

![nano](images/part7.2.1.png)
  |:--:|
![nano.2](images/part7.2.2.png)
![nano.3](images/part7.2.3.png)
![nano.4](images/part7.2.4.png)
| *Using NANO* |

  >to save & exit press control (^) + X and then type Y and press ENTER two times \
  >to exit without saving changes press control (^) + X and then type N and press ENTER \
  >search: Control (^) + W \
  >replace: Option (⌥) + R \

3. *==MCEDIT==_*

![mcedit](images/part7.3.1.png)
  |:--:|
![mcedit.2](images/part7.3.2.png)
![mcedit.3](images/part7.3.3.png)
![mcedit.4](images/part7.3.4.png)
| *Using MCEDIT* |

  >to save & exit fn+F10 and choose Yes \
  >to exit without saving changes fn+F10 and choose No \
  >search: fn+F7 \
  >replace: fn+F4

## Part 8. Installing and basic setup of the SSHD service

1. 
![installing ](images/part8.1.png)
  |:--:|
| *installing SSHd* |

2. 
![enabling ssh autostart](images/part8.2.png)
  |:--:|
| *enabling ssh autostart* |

3. 
![reset](images/part8.3.png)
  |:--:|
![reset.2](images/part8.4.png)
| *Resetting ssh ports to 2022* |

4. 
![ps](images/part8.5.png)
  |:--:|
| *showing sshd in procces via PID* |

`netstat -tan`
![netstat](images/part8.6.png)

> --numeric , -n to show network addresses as numbers \
>-a, --all to show status of all sockets \
>-t --tcp to display only tcp connections \

>Output Columns: \
>Proto - protocol used by the socket \
>Recv-Q - shows the number of bytes not copied by the program connected to the socket \
>Send-Q - shows the number of bytes not recognized (confirmed) by the remote host \
>Local Address - Local computer IP address and port number used Foreign Address - IP address and port number of the remote computer to which the socket is connected \
> State - socket status \
> 0.0.0.0 - This is a non-routable meta address that is used to identify an unknown or invalid target. In terms of servers, 0.0.0.0 means all IPv4 addresses on the local machine. In the case of a route entry, this means the default route \

## Part 9. Installing and using the top, htop utilities

uptime: 9 min \
user: 1 \
load average: 0.00, 0.02, 0.03 \
Tasks total: 94 \
%Cpu(s): 0,0, 0.0 sy, 0.0 ni, 100.0 id, 0.0 wa, 0.0 hi, 0.0 si, 0.0 st \
MiB Mem: 508.4 free, 144.8 used 323.7 buff/cache \
most %MEM pid: 641 \
most %CPU pid: 1

![htop](images/part9.1.png)
![htop.2](images/part9.2.png)
![htop.3](images/part9.3.png)
![htop.4](images/part9.4.png)
![htop.5](images/part9.5.png)

## Part 10. Using the fdisk utility

![fdisk](images/part10.1.png)

## Part 11. Using the df utility

Partition size: 4299472 \
Used: 3120460 \
Free space: 940012 \
Use%: 77 \
Units: 1Kb

_Human readable_
Partition size: 4.2G \
Used: 3.0G \
Free space: 918M \
Use%: 77% \
Type: ext4

## Part 12. Using the du utility

![du](images/part12.1.png)
![du.2](images/part12.2.png)
![du.3](images/part12.3.png)

## Part 13. Installing and using the ncdu utility

![ncdu](images/part13.1.png)
![ncdu.2](images/part13.2.png)
![ncdu.3](images/part13.3.png)


## Part 14. Working with system logs
Aug 10 18:23:38 user-1 by LOGIN

![restart_log](images/part14.1.png)

## Part 15. Using the CRON job scheduler

![cron](images/part15.1.png)
![cron.2](images/part15.2.png)
![cron.3](images/part15.3.png)
![cron.4](images/part15.4.png)
