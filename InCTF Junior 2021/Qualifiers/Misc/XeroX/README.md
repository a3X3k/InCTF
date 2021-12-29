# XeroX

### Challenge Description

> Things are not always what they seem, the intelligence of a few perceives what has been carefully hidden.

### Hints

- How do you find the difference between two files?
- Linux commands can be used....

### Solution 

- From the description and hints, its evident that something is either **identical/not identical** between the two images.
- Comparing the **hex chunks** of the images and concatenating all the **distinct chunks** gives the flag.

```js
cmp -l -b 1.jpg 2.jpg
```

```
178614 151 i     76 >
178697 156 n    323 M-S
178857 143 c     51 )
179080 164 t    307 M-G
179351 146 f     27 ^W
179797 173 {    112 J
180086 146 f    314 M-L
180343  61 1    333 M-[
180536 156 n    335 M-]
180857 144 d    331 M-Y
181034  61 1    152 j
181258 156 n    133 [
181497 147 g    364 M-t
181658 137 _    170 x
181784 144 d    115 M
182024  61 1    145 e
182231 146 f     63 3
182392 146 f    153 k
182536  63 3    314 M-L
182663 162 r    143 c
182856  63 3    304 M-D
183079 156 n    366 M-v
183288 143 c    266 M-6
183512  63 3    151 i
183625  65 5    312 M-J
183817 137 _     24 ^T
183992  61 1    312 M-J
184216  65 5    176 ~
184457 137 _    335 M-]
184665 156 n    126 V
184921  60 0    103 C
185306 164 t    317 M-O
185515 137 _     35 ^]
185787 164 t     14 ^L
186091 150 h    333 M-[
186411  64 4    304 M-D
186938 164 t     53 +
187482 137 _    135 ]
188267  63 3    130 X
188890  64 4    364 M-t
189578  65 5    165 u
190443 171 y    264 M-4
191242 175 }    110 H
```

### Flag

> inctf{f1nd1ng_d1ff3r3nc35_15_n0t_th4t_345y}

### Author

[S Abhishek](https://twitter.com/a3X3k)
