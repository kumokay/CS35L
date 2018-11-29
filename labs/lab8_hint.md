Answer 2 questions in the file hw.txt

Generate a key pair with the GNU Privacy Guard’s commands
`$ gpg --gen-key (choose default options)`

Export public key, in ASCII format, into hw-pubkey.asc 
`$ gpg --armor --output hw-pubkey.asc --export ‘Your Name’`

Make a tarball of the above files + log.txt and zip it with gzip to produce hw.tar.gz
```
$ tar –cf hw.tar <files>
$ gzip hw.tar -> creates hw.tar.gz
```

Use the private key you created to make a detached clear signature hw.tar.gz.sig for hw.tar.gz
`$ gpg --armor --output hw.tar.gz.sig --detach-sign hw.tar.gz `

Use given commands to verify signature and file formatting
These can be found at the end of the assignment spec  
