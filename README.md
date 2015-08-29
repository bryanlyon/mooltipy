# Mooltipy
A Mooltipass Python library and command line management utilities.

Under heavy development. I just got my unit ~ a couple weeks ago. This could be
called alpha stage work at the moment.

## Installation & Usage
You can install mooltipy using pip.
```
user@box:~/$ pip install mooltipy
```

### Add contexts
You can use mooltipass to add contexts. This is a terrible idea in practice
since you might log your password to .bash_history... but this should be
fixed soon with self-generating, random passwords.

```
$ sudo mplogin tripod.com --login=user_name --password="P@ssw0rd"
```

### Manage Data Contexts
The Mooltipass can be used to securely store small data files! Think ssh or gpg
keys and cryptocurrency wallets.

```
$ sudo mpdata import ssh_key ~/.ssh/id_rsa
$ sudo mpdata export ssh_key ./restored_key
```

### Using the Mooltipass module
To utilize the class:
```python
from mooltipy import MooltipassClient
import sys

mooltipass = MooltipassClient()

if mooltipass.ping():
    print('Connected to the mooltipass!')
else:
    print('Failed to connect to mooltipass.')
    sys.exit(0)

mootipass.do_limited_things()
```
