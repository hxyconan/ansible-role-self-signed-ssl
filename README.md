# ansible-role-self-signed-ssl

## Intro
- This is a role to install self signed certificate on Apache Ubuntu server
- Following the tutorial at [here](https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-apache-in-ubuntu-16-04) for Apache and SSL configuration

## Tested on
- Ubuntu 16.04 LTS
- Apache 2.4.7

## Pre-Installation Requirements
- Apache

## Verification
- Test the certificate configuration, You will see the pre-defined CN, expired date, SAN in the output
```sh
cd /etc/ssl/certs
openssl x509 -in EXAMPLE-cert.crt -text -noout
```


- Test the Apache vhost configuration via:
```sh
$ sudo apache2ctl configtest
Syntax OK
```

## Ref:
- Create self-signed certificate: 
-- http://blog.angrywombat.net/blog/2017/10/30/create-self-sign-ssl-certificate.html, see the Solution 2
- Configure ssl certificate in Apache on Ubuntu 16.04: 
-- https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-apache-in-ubuntu-16-04
- Generate Self-Signed SSL Certificate without prompt: 
-- https://gist.github.com/thbkrkr/aa16435cb6c183e55a33
-- https://www.shellhacks.com/create-csr-openssl-without-prompt-non-interactive/

