# The Numbers

- [The Numbers](#the-numbers)
  - [Challenge description](#challenge-description)
  - [Solution](#solution)
    - [Numbers to Letters](#numbers-to-letters)
  - [References](#references)

## Challenge description

```text
Level: Easy
Category: Cryptography
Author: Danny
Event: picoCTF 2019

Description:
The numbers... what do they mean?

Attachments:
the_numbers.png

Hints:
The flag is in the format PICOCTF{}
```

Challenge Link: [Challenge](https://learn.cylabacademy.org/library/68)

## Solution

### Numbers to Letters

When we open up the picture, we can see a bunch of numbers together with open and closed curly braces. If we match PICOCTF to the numbers on the picture, we can make this deduction:

text```
P (16th letter) -> 16
I (9th letter) -> 9
C (3rd letter) -> 3
...
```

The numbers actually correspond to the placing of letters in the alphabet.

Therefore, the solution can be found by converting the numbers into the corresponding letters.

text```
PICOCTF{<REDACTED>}
```

## References

 - [Types of ciphers](https://www.audiocipher.com/post/types-of-ciphers)
 - [a1z26 Cipher](https://planetcalc.com/4884/)
 - [a1z26 Cipher Decoder](https://cryptii.com/pipes/a1z26-cipher/)