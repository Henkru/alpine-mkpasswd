# mkpasswd

Use mkpasswd everywhere. Minimal alpine-based image with pre-installed mkpasswd.

## Usage

```
$ docker run -rm -it henkru/alpine-mkpasswd --method sha-512 --rounds 5000
Password:
$6$rounds=5000$7rImaEtgOP$6IfpeW0mNFTODkbgoXXiLfy0jzQgqeJyrudsOCe.AommJlpOjPzvvhoSSFkZVBQvuBpq27kkv4ROoVHY20mvi1
```

```
$ docker run -rm -it henkru/alpine-mkpasswd -h
Usage: mkpasswd [OPTIONS]... [PASSWORD [SALT]]
Crypts the PASSWORD using crypt(3).

      -m, --method=TYPE     select method TYPE
      -5                    like --method=md5crypt
      -S, --salt=SALT       use the specified SALT
      -R, --rounds=NUMBER   use the specified NUMBER of rounds
      -P, --password-fd=NUM read the password from file descriptor NUM
                            instead of /dev/tty
      -s, --stdin           like --password-fd=0
      -h, --help            display this help and exit
      -V, --version         output version information and exit

If PASSWORD is missing then it is asked interactively.
If no SALT is specified, a random one is generated.
If TYPE is 'help', available methods are printed.

Report bugs to <md+whois@linux.it>.
```
