


## Auth

```
users username[:pwtype:password] ...
pwtype is one of:
No password type: use system authentication.
CL - cleartext password
CR - crypt password, only MD5 crypt passwords are supported
NT - NT-hashed (MD4) passwords in hex, as used in pwdump or SAMBA
```

see https://3proxy.ru/howtoe.asp

crypt password generation example:
`openssl passwd -1 -salt SALT PASSWORD`
