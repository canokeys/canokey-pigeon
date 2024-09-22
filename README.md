# CanoKey Pigeon

## CA cert of FIDO

```
-----BEGIN CERTIFICATE-----
MIIBpzCCAUygAwIBAgIUatn9Rj8uCMjLrmFfCQYY5/X9xq4wCgYIKoZIzj0EAwIw
MTEvMC0GA1UEAwwmQ2Fub0tleXMgRklETyBBdHRlc3RhdGlvbiBSb290IENBIE5v
LjIwHhcNMjExMjI3MTE0OTMzWhcNNDEwNjI1MTE0OTMzWjAxMS8wLQYDVQQDDCZD
YW5vS2V5cyBGSURPIEF0dGVzdGF0aW9uIFJvb3QgQ0EgTm8uMjBZMBMGByqGSM49
AgEGCCqGSM49AwEHA0IABNgW7CwchH80l4sj8luhwjbNoohB9Uqnvsh0SLor18w8
IMy6rnzzdDP9PgSSbuUZw302mBhyYJqJY1q9Ke0niZujQjBAMB0GA1UdDgQWBBRU
GAKiwvk2vLP5Zi6ul73RiWyr0jAPBgNVHRMECDAGAQH/AgEAMA4GA1UdDwEB/wQE
AwIBBjAKBggqhkjOPQQDAgNJADBGAiEAlRNyrmngE3A1YZuwsuwBHLXY7wZC/4CO
JNA30mtp2+YCIQDA88Pp+Kjx3c4nrgRgSaSueC5IlvwpTSGBGwRYDSdMTA==
-----END CERTIFICATE-----
```

## Changelog

### 2.0.1
1. FIDO: Solve the problem of registration failure on the new version of Firefox. Specifically, do not return a map when the extension map is empty to avoid deserialization errors in the library used by Firefox (mozilla/authenticator-rs#317).

### 2.0.0
1. FIDO: Updated to FIDO version 2.1, supporting Credential Management, Credential Protection, Credential Blob, and Large Blob Key features, fixed a key generation bug (#19)
2. PIV: Supports configuring key properties (whether touch is required, whether PIN verification is required), added two sets of keys 82/83, supports some metadata to enhance compatibility.
3. OpenPGP: Supports RSA3072/4096 algorithms, fixed the issue of the first ED25519 signature error after power-on.
4. OATH: Supports returning the complete hash result.

### 1.6.2

1. Add an option for enabling the tailing enter when inputing the HOTP code.
2. Allow public keys with e != 65537.

### 1.6.1

1. Fix: USB is not reset when rebooting.
2. Increase the max size of certificate to 3000 bytes.

### 1.5.2

1. Canokey Pigeon first official version.
