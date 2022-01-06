# Panopto

## Challenge Description 

> Alice is searching for hidden treasure by traveling from region to region. Can you help her in finding the treasure?

## Solution

- Scan the given QR Code which gives the **Base32** decoding python script along with the URL.

```py
# Python / Python2 / Python3

# Run the following script along with the Base32 Encoded Gold to get the flag :)

# You can get the base32 gold from https://mega.nz/folder/dVJx3SKR#U_Dsjp10uLMspiJOXqyQjA

import base64

Base_32_Gold = "" # Enter the Base32 Gold within the double Quotes ("")

print(base64.b32decode(Base_32_Gold).decode("utf-8"))
```

- The URL redirects to the page where there are 3 images given.
- Among the 3 images, one of the image has the Base32 encoded text embedded as a **ZIP** file in it.
- Using `Binwalk` the file can be extracted from the Image and this can be understandable from the hint given in the challenge description.

```py
Binwalk Gold.png
```

- The extracted **Gold.zip**, has the **Gold.txt** file in it.

```
# Here is Base32 Gold

NFXGG5DGNJ5XUYRUOIYW4Z27GRXGIX3CGQ2TGXZTGJPWIM3DGBSDC3THL5TTC5RTONPXI2BTL5TGYNDHPU======
```

- After decoding the Base32 text given in the **Gold.txt**, the final flag will be visible.

### Flag

> inctfj{zb4r1ng_4nd_b453_32_d3c0d1ng_g1v3s_th3_fl4g}

