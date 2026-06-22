***Subnet ID***
You are looking for 1st address on network
If you get an IP & subnet mask -

| 165.     | 245.     | 77.      | 14    |
| -------- | -------- | -------- | ----- |
| **255**. | **255.** | **240.** | **0** |
| **165.** | **245.** | **X.**   | **0** |

For X : 
256 - 240 = 16 (This means 16 hosts per subnet) (16 is the magic number) 
0, 16, 32, 48, 64, 80 (Go up by 16)
77 $\rightarrow$ is the number and it is between the numbers 64 & 80 so we choose 64

==165.245.64.14==

******

***Broadcast Address***
You are looking for last address on the network
If you get IP & subnet mask -

| 165.     | 245.     | 77.      | 14      |
| -------- | -------- | -------- | ------- |
| **255**. | **255.** | **240.** | **0**   |
| **165.** | **245.** | **Y.**   | **255** |

For Y :
256 - 240 = 16 (This means 16 hosts per subnet) (16 is the magic number) 
0, 16, 32, 48, 64, 80 (Go up by 16)
77 $\rightarrow$ is the number and it is between the numbers 64 & 80 so we choose 80 (then - 1)
79 is the broadcast address

==165.245.79.255==

******

***1st Host***
Subnet ID + 1 : ==165.245.64.1==


***Last Host***
Broadcast Address - 1 : ==165.245.79.254==


******
