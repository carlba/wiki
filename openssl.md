# OpenSSL

## Usage

### Convert PEM to DER certificate

```bash
openssl x509 -outform der -in certificate.pem -out certificate.der
```


### Check DER certificate

```bash
openssl x509 -outform der -in certificate.pem -text -noout

```

### Convert chained PEM certificate to PKCS#7/P7B Format

```bash
openssl crl2pkcs7 -nocrl -certfile birdstep.internal.chained.cert -out birdstep.internal.chained.p7b
```

### Generate self signed certificate in PEM format

```bash
openssl req -new -newkey rsa:2048 -days 365 -nodes -x509 -keyout server.key -out server.crt
```
