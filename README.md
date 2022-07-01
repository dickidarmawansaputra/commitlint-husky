<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>
<p align="center"><a href="https://commitlint.js.org/" target="_blank"><img src="https://commitlint.js.org/assets/commitlint.svg" width="400"></a></p>

## Implement CommitLint -Husky with Laravel

``commitlint`` helps your team adhering to a commit convention. By supporting npm-installed configurations it makes sharing of commit conventions easy.
Husky improves your commits and more 🐶 woof!

- [CommitLint](https://commitlint.js.org/).
- [Husky](https://typicode.github.io/husky).

## Install commitlint

```
# Install and configure if needed
npm install --save-dev @commitlint/{cli,config-conventional}
# For Windows:
npm install --save-dev @commitlint/config-conventional @commitlint/cli

# Configure commitlint to use conventional config
echo "module.exports = { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
```

## Install husky

```
# Install Husky v6
npm install husky --save-dev
# or
yarn add husky --dev

# Activate hooks
npx husky install
# or
yarn husky install
```

