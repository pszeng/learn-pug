# learn-pug

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Run your unit tests

```
npm run test:unit
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

### 集成 pug 模板

npm i -D pug pug-html-loader pug-plain-loader

vue.config.js 配置如下：
module.exports = {
chainWebpack: config => {
config.module.rule('pug')
.test(/\.pug\$/)
.use('pug-html-loader')
.loader('pug-html-loader')
.end()
}
}
