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

## Add hook

```
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'
```

Make hook executable

```
chmod a+x .husky/commit-msg
```

## Test the hook

```
git commit -m "foo: this will fail"
husky > commit-msg (node v10.1.0)
No staged files match any of provided globs.
⧗   input: foo: this will fail
✖   type must be one of [build, chore, ci, docs, feat, fix, perf, refactor, revert, style, test] [type-enum]

✖   found 1 problems, 0 warnings
ⓘ   Get help: https://github.com/conventional-changelog/commitlint/#what-is-commitlint

husky > commit-msg hook failed (add --no-verify to bypass)
```

```
git commit -m "chore: lint on commitmsg"
```

