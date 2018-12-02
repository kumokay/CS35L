Answer 2 questions in the file hw.txt

Generate a key pair with the GNU Privacy Guard’s commands
```
$ gpg --gen-key (choose default options)
```

Export public key, in ASCII format, into hw-pubkey.asc 
```
$ gpg --armor --output hw-pubkey.asc --export ‘Your Name’
```

Use the private key you created to make a detached clear signature for eeprom
```
$ gpg --armor --output your_sig --detach-sign your_eeprom
```

Use given commands to verify signature and file formatting
These can be found at the end of the assignment spec  
