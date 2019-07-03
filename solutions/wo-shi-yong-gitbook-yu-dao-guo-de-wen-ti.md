# 我使用gitbook遇到过的问题

## 安装后首次运行 `gitbook init` 报错

报错信息如下：

```text
Error loading version latest: Error: Cannot find module 'debug'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:582:15)
    at Function.Module._load (internal/modules/cjs/loader.js:508:25)
    at Module.require (internal/modules/cjs/loader.js:637:17)
    at require (internal/modules/cjs/helpers.js:22:18)
    at Object.<anonymous> (/Users/song/.gitbook/versions/3.2.3/node_modules/nunjucks/node_modules/chokidar/node_modules/readdirp/node_modules/micromatch/node_modules/snapdragon/lib/compiler.js:5:13)
    at Module._compile (internal/modules/cjs/loader.js:701:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:712:10)
    at Module.load (internal/modules/cjs/loader.js:600:32)
    at tryModuleLoad (internal/modules/cjs/loader.js:539:12)
    at Function.Module._load (internal/modules/cjs/loader.js:531:3)

TypeError: Cannot read property 'commands' of null
```

找不到依赖库 `debug`，解决思路为找到gitbook安装目录重新安装依赖库：

1. 运行`cd  ~/.gitbook/versions/3.2.3/`
2. 运行 `rm -rf node_modules && npm install`

`npm install` 运行成功后，再次运行`gitbook init`，产生了新的报错信息

```text
Error loading version latest: Error: Cannot find module 'source-map'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:582:15)
    at Function.Module._load (internal/modules/cjs/loader.js:508:25)
    at Module.require (internal/modules/cjs/loader.js:637:17)
    at require (internal/modules/cjs/helpers.js:22:18)
    at Object.<anonymous> (/Users/song/.gitbook/versions/3.2.3/node_modules/nunjucks/node_modules/chokidar/node_modules/readdirp/node_modules/micromatch/node_modules/snapdragon/lib/utils.js:8:21)
    at Module._compile (internal/modules/cjs/loader.js:701:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:712:10)
    at Module.load (internal/modules/cjs/loader.js:600:32)
    at tryModuleLoad (internal/modules/cjs/loader.js:539:12)
    at Function.Module._load (internal/modules/cjs/loader.js:531:3)

TypeError: Cannot read property 'commands' of null
```

这次是找不到依赖库`source-map`， 看了下package.json，里面没有添加这个依赖库， 安装一个

* 运行`npm install source-map`

安装成功后，运行`gitbook init` 成功，问题解决。

**我猜测安装gitbook3.2.3版本都会遇到这个问题，卸载重装果然复现了这个问题。 在terminal运行以下命令可以快速解决这个问题**

`cd ~/.gitbook/versions/3.2.3/ && npm install source-map debug`

