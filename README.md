# README

## Initialize conventional commits with linting using husky hooks

install required libraries

```bash
npm install --save-dev @commitlint/{cli,config-conventional,prompt-cli}
```

Configure commitlint to use conventional config

```bash
echo "module.exports = { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
```

Install `husky` as devDependency, a handy git hook helper available on npm.

```bash
npm install husky --save-dev
```

Now activate husky hooks

```bash
npx husky install
```

add commit message hook

```bash
npx husky add .husky/commit-msg  'npx --no -- commitlint --edit ${1}'
```

Reference: https://commitlint.js.org/#/guides-local-setup
