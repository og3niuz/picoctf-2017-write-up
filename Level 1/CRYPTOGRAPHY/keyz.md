# keyz
___
### Question
While webshells are nice, it'd be nice to be able to login directly. To do so, please add your own public key to ```~/.ssh/authorized_keys```, using the webshell. Make sure to copy it correctly! The key is in the ssh banner, displayed when you login remotely with ssh, to ```shell2017.picoctf.com```

### Hint
 - There are plenty of tutorials out there. This one covers key generation: https://confluence.atlassian.com/bitbucketserver/creating-ssh-keys-776639788.html
 - Then, use the web shell to copy/paste it, and use the appropriate tool to ssh to the server using your key
___
### Solution
It's basic ssh setup.
Steps:
1. Open Terminal, and create ssh keys. Give password if you want.
    ``` ssh-keygen -t rsa -b 4096 ```
2. Copy id_rsa.pub to your clipboard.
3. Open webshell of picoctf and create a file called ```authorized_keys``` in ```~/.ssh/```
    ``` vim ~/.ssh/authorized_keys ```
4. Paste the public key from the clipboard.
5. SSH the shell2017.picoctf.com server.
```bash 
    ssh username@shell2017.picoctf.com -i id_rsa
    Congratulations on setting up SSH key authentication!
    Here is your flag: who_needs_pwords_anyways
```

___
___

Thanks

Twitter : [@iammrdollar](https://twitter.com/iammrdollar)

Github : [@iammrdollar](https://github.com/iammrdollar)
