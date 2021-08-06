# Commit Rule Config Demo Docs

## Commitizen

[Commitizen Docs](http://commitizen.github.io/cz-cli/)

### 安装

```sh
yarn add --dev commitizen
```

### 初始化适配器

```sh
npx commitizen init cz-conventional-changelog --save-dev --save-exact
```

### 添加 commit 脚本

```json
"scripts": {
  "commit": "cz"
}
```

## commitlint

### 安装 commitlint

```sh
yarn add -D @commitlint/{cli,config-conventional}
```

### 配置 commitlint.config.js

```sh
echo "module.exports = { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
```

## Husky

### install husky

```sh
npm install husky --save-dev
```

### 启动 git hooks

```sh
npx husky install
```

### 要在安装后自动启用 Git 挂钩，请编辑 package.json

npm set-script prepare "husky install"

### 添加 hooks

```sh
npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
```
