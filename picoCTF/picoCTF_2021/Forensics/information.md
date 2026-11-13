# information

- [information](#information)
  - [Challenge description](#challenge-description)
  - [Solution](#solution)
    - [Metadata](#metadata)
  - [References](#references)

## Challenge description

```text
Level: Easy
Category: Forensics
Author: susie
Event: picoCTF 2021

Description:
Files can always be changed in a secret way. Can you find the flag?

Attachments:
cat.jpg

Hints:
1. Look at the details of the file
2. Make sure to submit the flag as academy{XXXXX}
```

Challenge Link: [Challenge](https://learn.cylabacademy.org/library/186)

## Solution

### Metadata

In this challenge, we are given a picture of a cat. The flag is somewhere inside the picture, but it is not obvious when we first look at the picture. This is where we would need to use tools that can check the file's metadata for clues or the flag itself.

The metadata of a file provides context, structure, and details that describe, explain, or locate an information resource without necessarily containing the core content itself. This is a very common place for people's information to appear, or in this case, the flag. Therefore, we can use metadata viewing tools to uncover hidden data.

One of these tools is [Aperisolve](https://www.aperisolve.com/), a online tool that provides the metadata of a picture and many more tools all in one website. It is a extremely important tool for digital forensics regarding pictures. To use the tool, simply insert your picture into the website and it will automatically give you all the details about the picture.

After scrolling down to the Exiftool section, which is a section named after the Linux command used to view the metadata of a file, we can see a suspicious "License" key that holds the value:

```text
YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
```

Upon first look, we can immediately tell that this is encoded with base64 encoding, thus we can use another online tool to decrypt the cipher and get the result, which is coincidentally the flag.

## References

 - [Metadata](https://graphwise.ai/fundamentals/what-is-metadata/)
 - [Aperisolve](https://www.aperisolve.com/)
 - [Exiftool](https://en.wikipedia.org/wiki/ExifTool)
 - [CyberChef](https://gchq.github.io/CyberChef)
 - [Base64](https://en.wikipedia.org/wiki/Base64)
 - [Linux](https://en.wikipedia.org/wiki/Linux)