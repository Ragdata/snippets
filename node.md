# Node.js Snippets

## 📖 Index / Table of Contents

* [HOME](https://github.com/Ragdata/snippets)
  * [git-crypt](git-crypt.md)
  * [gpg](gpg.md)
  * [Node.js](node.md)

## Generate 'Secret' Hash

````bash
node -e "console.log(crypto.randomBytes(32).toString('hex'))"
````
