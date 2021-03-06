nodejs npm

# [Node.js](https://nodejs.org/en/)
## Install
### Linux - Install latest version
`Ubuntu` package manager doesn't have the latest version. To install:
- install [NVM](https://github.com/nvm-sh/nvm) *(Node Version Manager)*
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
Running the script first without the `| bash` will show what the script will do

- Restart Terminal
- Check installation
```
nvm --version
```
- install latest version
```bash
nvm install 16.14
```

## Uninstall npm packages
https://nodejs.dev/learn/uninstalling-npm-packages

```bash
npm uninstall --save <package_name>
```
- `--save` will remove package from `package.json`
