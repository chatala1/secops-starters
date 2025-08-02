---
title: HTB Guide - Sandworm
layout: home
parent: <b>Hack The Box</b>
---

# Sandworm
![Sandworm](https://github.com/chatala1/htb-writeup/assets/16328550/1f665c88-6003-40c9-bb22-7718abdf12d8)
## Overview
* Target IP **10.10.11.218**
* Released on 17 Jun 2023
<br>

## Walkthrough
<br>

### Access the host
---

1. Scan the network
```
sudo nmap -A -sC-sV --reason -v 10.10.11.218
```
<br>
2. Add the ssa.htb domain to the hosts file

```
sudo nano /etc/hosts
```
<br>
3. Open https://ssa.htb in your browser

* https://ssa.htb/admin
* https://ssa.htb/guide
* https://ssa.htb/login
* https://ssa.htb/pgp 👈
<br>

4. Copy the PrettyGoodPrivacy key from the https://ssa.htb/pgp page
<br>

5. Place the PGP Key into the corresponding box and click to verify the signature

PGP Page Legend

| Public Key | Conversion Type |
|---|---|
| Encrypted Text | Decrypted Message |
| Public Key | Encrypted Message |
| Public Key | Signed Text |

6.Place the PGP Key into the Public Key box next to 'Encrypted Message'.
<br>

7. Copy the resulting message from the previous step. Paste it into the Encrypted Text box. Click Decrypt Message.

<br>
### Flask Exploit Discovery


<br>
8.Research Flask Exploits. Maybe try SSTI.

<br>
### Generate a key

9. Create a private key

```
gpg --gen-key
```

* Real Name: {{7*7}}
* Email: test@test.org
<br>

10 . Export and verify the key

```
gpg --armor --export test@t.t
```


```
cat pubkey.asc
```

<br>
### Signing Message

```
echo "aa a" | gpg --clear-sign -u test@t.t
```
```
cat payload.txt test
```
```
gpg --clear-8098809sign --output signedmessage.asc payload.txt
```

<br>
### Exploit

<br>
### Reverse Shell

<br>
### Create New Ticket

<br>
### Verify Signature

<br>
### Silent Observer

<br>
### Checking the Source

<br>
### Another file

<br>
### Exploit file

<br>
### Copy Exploit file

<br>
### Run Program

<br>

