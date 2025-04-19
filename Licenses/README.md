# Licenes

Software and service may require a license in the form of a token or file.
These can be captured here. Ansible Vault can be used to encrypt these
licences either plain text or binary.

## Historical Record

Also note that older versions of files are easy to locate in Git history.

``` bash
git log file_you_want_prior_version_of
commit <unique identifier>
Author: Who commited it
Date: When it was done including timestamp and timezone

    <the mesg used when commiting it>

commit <unique identifier>
Author: Who commited it
Date: When it was done including timestamp and timezone

    <the mesg used when commiting it>

commit <unique identifier>
Author: Who commited it
Date: When it was done including timestamp and timezone

    <the mesg used when commiting it>

commit <unique identifier>
Author: Who commited it
Date: When it was done including timestamp and timezone

    <the mesg used when commiting it>
```

When you have the unique identifier you want then you can show the file like:

``` bash
git show <unique identifier>:file_you_want_prior_version_of
```

Please note the colon used to seperate the id from filename.

## Keys and Tokens

- Vendor Software Package X
  - Current key: [example.vendor.product.lic](example.vendor.product.lic)
  - Changelog:
    - Renew: 2025-04-02 to 2028-02-02 by Bill

## Encryption / Decryption

Ansible Vault is easy to use once setup method to secure keys or tokens.

### Encryption

```bash
cd Infrastructure/
ansible-vault encrypt ../Licenses/example.vendor.product.lic
Encryption successful
```

### Decryption aka view

```bash
cd Infrastructure/
ansible-vault view ../Licenses/example.vendor.product.lic
Product: XYZ
Key: TJaMIG0MRQwEgYDVQQKEwtFbnRydXN0Lm5ldDFA
```

### Binary Files

In Ansible roles and playbooks binary files can be encrypted also. This can be
done on the command line interface with the pattern above.

```bash
ansible-vault encrypt ../Licenses/example.vendor.product.lic.tar.gz 
Encryption successful
```

The file can not be viewed, it must instead be decrypted

```bash
ansible-vault decrypt ../Licenses/example.vendor.product.lic.tar.gz 
Decryption successful
```

Be careful not to check in the decrypted version by accident.
