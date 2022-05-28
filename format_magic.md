# format_magic solution

## by mario

## Premise:
This challenge is in the steganography/miscellaneous category. This means that we are tasked with finding hidden information or data within something else (To learn more about  steganography, the wiki can be [found here](https://en.wikipedia.org/wiki/Steganography)). The only file we are provided with in this challenge is a jpg image [format_magic.jpg.](http://chal.ctf-league.osusec.org/format_magic.jpg)

## First Step:
Being that this is a steganography challenge, we know that there must be some hidden data in the image given to us. There are many steganography tools that can be used to find hidden files inside other files. The one that I used for this challenge is called Binwalk. [Binwalk](https://www.kali.org/tools/binwalk/) allows us to scan a file and see if any other files are also contained within the original file. If we run binwalk with the “-B” flag, it will scan a file for file signatures and report what other file types it can find. We can use this utility on the supplied image by running “binwalk -B format_magic.jpg” and get the following output:

![binwalk 1](/m-schmutz/CTF-Writeups/blob/main/format_magic_images/binwalk_1.png?raw=true "binwalk 1")

