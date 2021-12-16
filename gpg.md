# GPG Snippets

## 📖 Index / Table of Contents

* [HOME](README.md)
  * [git-crypt](git-crypt.md)
  * [gpg](gpg.md)
  * [Node.js](node.md)

## Create GPG Key

````bash
gpg --gen-key
````

## List Keys

````bash
gpg --list-secret-keys
gpg --list-keys
````

## Export Key

````bash
gpg --export --armor $KEY_ID
````

## Import Key

````bash
gpg --import /path/to/file
````
