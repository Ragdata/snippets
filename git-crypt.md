# git-crypt Snippets

🔐 git-crypt is a tool to help you keep secrets safe in git repositories

## 📖 Index / Table of Contents

* [HOME](README.md)
  * [git-crypt](git-crypt.md)
  * [gpg](gpg.md)
  * [Node.js](node.md)

## Install git-crypt
````bash
sudo apt-get install -y git-crypt
````

## Initialise git repository
````bash
git init
git-crypt init
````

## Setup git-crypt

Add a `.gitattributes` file to the root directory your repository and define which files should be encrypted:

````bash
secrets.txt filter=git-crypt diff=git-crypt
*.key filter=git-crypt diff=git-crypt
secretdir/** filter=git-crypt diff=git-crypt
````

It is good practice to add a line to prevent encrypting the `.gitattributes` file itself:

````bash
.gitattributes !filter !diff
````

## Add a Trusted GPG Key

````bash
git-crypt add-gpg-user --trusted ragdata@users.noreply.github.com
````

## Test Encryption

````bash
git-crypt status -e
````

## Unlock Encrypted Files

````bash
git-crypt unlock
````
