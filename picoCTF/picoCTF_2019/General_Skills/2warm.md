# 2warm

- [2warm](#2warm)
  - [Challenge description](#challenge-description)
  - [Solution](#solution)
    - [Background](#background)
    - [Flag](#flag)
  - [References](#references)

## Challenge description

```text
Level: Easy
Category: General Skills
Author: Sanjay C/Danny Tunitis
Event: picoCTF 2019

Description:
Can you convert the number 42 (base 10) to binary (base 2)?

Hints:
1. Submit your answer in our competition's flag format. For example, if your answer was '11111', you would submit 'academy{11111}' as the flag.
```

## Solution

### Background

Numbers can be expressed in many different forms. The current numeric system that we commonly use is the base-10 numeric system, which consists of numbers 0-9. In other bases, the number of digits that are used corresponds to the base of the system.

In this challenge, we are required to convert the number 42 in base-10 to base-2, also known as binary.

Base-2 is a numeric system that uses two digits, 0 and 1. Just like in base-10 where we have to use two digits instead of 1 to represent 9 + 1, we would also need to use two digits to represent 1 + 1 in base-2. Both of these would produce the number 10, but one of them means 10 while the other means 2.

In base-10, the more digits you use corresponds to a larger denomination of 10. If the ones place increments by 10^0, the tens place increments by 10^1, the hundreds place increments by 10^2 and so on. This corresponds to the base-2 system, where the first digit increments by 2^0, the second digit increments by 2^1, the third digit increments by 2^2 and so on.

To calculate 42 in base 2, we first find the greatest denomination of 2 that can subtract with this number and still get a posiitve result. For example:

```text
42 - 64 (2^6) = -22 (Not positive)

42 - 32 (2^5) = 10 (Is positive)
```

We then repeat until the final positive result is exactly 0. 

```text
42 - 32  -  8  -  2 = 0
    (2^5) (2^3) (2^1)
```

Then, for every denomination used in the calculation, we put a 1 in that place instead of a 0.
The final answer should look like this:

```text
101010
```

Therefore, 42 in base-10 is 101010 in base-2.

### Flag

```text
picoCTF{101010}
```

## References

 - [Cyberchef](https://gchq.github.io/CyberChef/)
 - [Binary](https://en.wikipedia.org/wiki/Binary_number)
 - [Decimal](https://en.wikipedia.org/wiki/Decimal)