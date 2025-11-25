# HoneyPot_Lite

## Install

1) Clone repository.

```
git clone https://github.com/Vivin-K-R/HoneyPot_Lite.git
```

2) Key generation

An RSA key must be generated for the SSH server host key. The SSH host key provides proper identification for the SSH server. Ensure the key is named `server.key` and resides in the same relative directory as the honeypot.

```
ssh-keygen -t rsa -b 2048 -f server.key
```

3) Run

Make sure you run this in a virtual environment and have all the dependencies installed (see requirements.txt).

To start the HTTP honeypot:

```
python3 run_honeypot.py -a 127.0.0.1 -p 2223 -u admin -pw admin --http
```

To start the SSH honeypot:

```
python3 run_honeypot.py -a 127.0.0.1 -p 2223 -u admin -pw admin --ssh
```

Then, from a shell you can connect to the fake SSH server with:

```
ssh admin@127.0.0.1 -p 2223
```

## Environment

- Windows 11 (recommended: run inside a VM for security)
- Visual Studio Code
- Python 3
- Ubuntu 22.04 LTS
