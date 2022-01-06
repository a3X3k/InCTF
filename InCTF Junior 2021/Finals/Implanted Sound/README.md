# Implanted Sound

### Challenge Description 

> Driving in reverse gear may be necessary when you are stuck in a narrow lane or a road with a dead end! 
> Always remember that each of the lowercase alphabets and numbers in the traffic signs have their own unique dot-dash code.
> Flag format : inctfj{diamond_gold_silver}

### Solution 

- From the challenge description we can get a hint that, `Binwalk` has to be used to extract some files from the **Horror.jpg**.

```py
binwalk Horror.wav
```

- Using binwalk the hidden **Horror.wav** can be extracted.
- Initial analysis would be **Morse Code** translation, but it doesn't make any sense.
- The challenge **description** as well as the image hints that there is some thing to be **reversed**.
- **Reverse** the audio and try for **Morse Code** to get the flag.

### Flag

> inctfj{15n't_m0r53_c00l??}
