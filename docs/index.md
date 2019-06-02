# 快速开始
推荐安装 `docsify-cli` 工具，可以方便创建及本地预览文档网站。
```
npm i docsify-cli -g
```

# 初始化项目
如果想在项目的 `./docs` 目录里写文档，直接通过 `init` 初始化项目。

```
docsify init ./docs
```

# 开始写文档
## 单页面
* `index.html`是入口文件
* `README.md`会作为主页内同渲染，不过是可以配置的东西
* `.nojekyll`用于阻止 GitHub Pages 会忽略掉下划线开头的文件
## 多页面
自己简单配置的一个配置文件：
```
    window.$docsify = {
      name: 'for-docsify',
      nameLink: '/',
      homepage: 'index.md',
      loadSidebar: 'guide.md',
      subMaxLevel: 2,
      auto2top: true,
      themeColor: '#3F51B5',
      mergeNavbar: true,
      formatUpdated: '{MM}/{DD} {HH}:{mm}',
      repo: 'https://github.com/1549469775/for-docsify'
    }
```
该配置文件修改之后侧边栏是`guide.md`生成的，主页是`index.md`，侧边栏标题是`for-docsify`，右上角有一个跳转`github`链接，只要把`repo`改了就成。
> 配置文件不用去记，要用的时候查一下api就行了

# 本地预览网站
```
docsify serve docs
```