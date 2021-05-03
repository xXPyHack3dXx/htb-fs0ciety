# fs0ciety
Solution to Hack The Box Challenge - fs0ciety

### Problem

We believe that there is an SSH Password inside password protected 'ZIP' folder. Can you crack the 'ZIP' folder and get the SSH password?

### Solution

Using [fcrackzip](http://manpages.ubuntu.com/manpages/precise/en/man1/fcrackzip.1.html) you can bruteforce a zip file giving a dictionary.

```bash
fcrackzip -u -v -D -p dictionary.txt password.zip 
```

I used the [ohmama wordlist](https://github.com/xXPyHack3dXx/wordlist/blob/master/passwords/ohmama.zip)

After that you will get the password to open the .txt file. Inside of it there is a phrase cyphered.

With this [tool](https://www.dcode.fr/cipher-identifier) you can detect what cypher was used. That detects that is base64, with the same tool you can decrypt it...

You will get some binary code, use any binary to text translate and you have the flag...





