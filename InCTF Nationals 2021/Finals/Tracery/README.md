# Tracery

## Challenge Description

> Do you know any communications standard which enables to exchange messages over a network.
- Flag format : inctf{}

## Solution 

- When analysing the packets we shall find that there are some texts sent as payload data.

```
If you are searching for something, I can give you that. Here is my password
```

- The following packets contains payload data as **Length?**.
- Each packet length is varying and all those packets length is **< 200**. 
- From the hint we have we shall try converting the length of the packet to ascii characters which gives some text. 

```
i 105
n 110
c 99
t 116
f 102
{ 123
1 49
_ 95
4 52
m 109
_ 95
n 110
0 48
t 116
_ 95
t 116
h 104
3 51
_ 95
f 102
l 108
4 52
g 103
_ 95
g 103
0 48
t 116
_ 95
1 49
t 116
? 63
? 63
} 125
```

```
inctf{1_4m_n0t_th3_fl4g_g0t_1t??}
```

- On further analysing, we shall find some more texts.

```
I can also give you something more!!
```

- The following packet's payload data shows that the **PDF** has been sent in the remaining packets and all those packets are of length **> 200**.
- Using scapy we shall extract the **password** and the **PDF**.

> <span style="color:red">**Use python2**</span>.

```py
from __future__ import print_function
from scapy.all import *

r=rdpcap("1.pcap")
a=open("Out.pdf","wb")

d=""

for i in range(len(r)):

    b=len(r[i][TCP].payload)
    
    if(b<200):
    
        print(chr(b),end="")
        
    if(b>200):
    
        c=r[i][TCP].payload
        d=d+str(c)
        
a.write(d)
a.close()
```

- The PDF is password protected and we have only one text with us right now.
- Decrypting the PDF file using **inctf{1_4m_n0t_th3_fl4g_g0t_1t??}** as a password gives us the flag.

## Flag

> inctf{Y4yy_5ubm1tt_m33_n0ww!!}

## Authors

[S Abhishek](https://twitter.com/a3X3k) & [Sampath](https://twitter.com/Sampath53509318)
