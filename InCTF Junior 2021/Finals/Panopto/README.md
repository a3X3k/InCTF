## Chall name 

> Panopto

## Chall Desc 

> Alice is searching for hidden treasure by traveling from region to region. Can you help her in finding the treasure?

## Write up

Scan the given QR Code using `zbarimg`

`zbarimg Gold.png`

It will give the `Base32` decoding python script along with the URL where the Base32 encoded text is present.

The URL redirects to the page where there are 3 images given.

Among the 3 images, one of the image has the Base32 encoded text embedded as a `ZIP` file in it.

Using Binwalk the file can be extracted from the Image.

`Binwalk Gold.png`

Now you will get a `Gold.zip`, which has the `Gold.txt` file in it.

`Gold.txt` file has the Base32 encoded text, `NFXGG5DGNJ5XUYRUOIYW4Z27GRXGIX3CGQ2TGXZTGJPWIM3DGBSDC3THL5TTC5RTONPXI2BTL5TGYNDHPU======`

After decoding this from Base32, the final flag will be visible.

### Flag - inctfj{zb4r1ng_4nd_b453_32_d3c0d1ng_g1v3s_th3_fl4g}

