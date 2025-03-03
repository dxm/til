# Fix Gpg Keyboxd Error

If _~/.gnugpg_ does not exist, keyboxd will be started. If you remove
this directory, keyboxd needs to be killed.

> If the ~/.gnupg home directory does not exist, the keyboxd is now automagically enabled.

> Since version 2.4.1 the keyboxd will be used by default for a fresh install; i.e. if a ~/.gnupg directory did not yet exist.

- [2203147 – gpg: key generation failed: Attempt to write a readonly SQL database](https://bugzilla.redhat.com/show_bug.cgi?id=2203147)
- [rGd9e7488b17fd](https://dev.gnupg.org/rGd9e7488b17fdc617eec735e2c0485b69285ba511)

```bash
$ gpgconf --kill keyboxd
```
