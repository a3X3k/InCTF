# Tracery

### Challenge Description

- Do you know any communications standard which enables to exchange messages over a network.
- Flag format : inctf{}

**Challenge File**

+ [Primary Link]()

### Short writeup

- Follow the TCP Stream and get the hint about the length.
- Converting the length to ascii gives the Password.
- We get the password protected PDF file from the TCP payload.
- Decrypting and opening it with the password gives the flag.

### Flag

inctf{Y4yy_5ubm1tt_m33_n0ww!!}

### Authors

[S Abhishek](https://twitter.com/a3X3k)
[Sampath](https://twitter.com/Sampath53509318)