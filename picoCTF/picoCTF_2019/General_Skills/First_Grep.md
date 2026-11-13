# First Grep

- [First Grep](#first-grep)
  - [Challenge description](#challenge-description)
  - [Solution](#solution)
    - [Grep](#grep)
    - [Flag](#flag)
  - [References](#references)

## Challenge description

```text
Level: Easy
Category: General Skills
Author: Alex Fulton/Danny Tunitis
Event: picoCTF 2019

Description:
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way. The flag is in this file.

Attachments:
file

Hints:
1. grep tutorial
```

Challenge Link: [Challenge](https://learn.cylabacademy.org/library/85)

## Solution

### Grep

Grep is a linux command that can find all occurences of a specific phrase in specified documents. Here is how do use grep:

```text
grep <options> "pattern" <file_name>
```

### Flag

As we know the flag always starts with academy, we can input this command into the linux terminal:

```text
grep "academy" file
```

Below is the output of this command:

```text
$ grep "academy" file

,6ZMyCV7QFRZ8E       >Vacademy{<REDACTED>}
```

## References

 - [Grep](https://en.wikipedia.org/wiki/Grep)
 - [Grep manual](https://man7.org/linux/man-pages/man1/grep.1.html)
 - [Linux command line](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview)