#Simple password manager

spm is a simple bash script that allows you to store passwords in a 'user@domain password' format.
spm is designed to be *exceptionally* simple, so it is limited to 100 LOC. 
Passwords and their domains are encrypted with a symmetric AES cipher.

Password storage is located at `$HOME/.local/spm`

## PSA 
spm is a simple script that provides a (very) limited interface to a bunch of openssl functions. That said, it *still* is a password manager and, as such, it HAS NOT BEEN AUDITED. Use with caution. 

##Prerequisites

spm requires openssl for encryption/decryption and apg for password generation.

##User guide

Add new record:

    $ spm new login domain

List all records (without passwords):

    $ spm ls [filter]

List all records (with passwords):

    $ spm export

Remove record:

    $ spm rm login@domain

Display password for a record:

    $ spm login@domain

