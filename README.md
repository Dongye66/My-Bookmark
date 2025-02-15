# 偶像练习生的膻味书屋

由于我喜欢收集各种实用或者稀奇古怪的网站，而如何存放它们成了一个问题，于是就有了这个在线的书签网站

## 我的在线网页
https://web.okarin.cn/

## 如何在本地运行

克隆项目到本地
```
git clone https://github.com/Okarin1/web-project.git
```
安装依赖
```
yarn install
```
本地运行
```
yarn serve
```

## 如何更换内容

在项目的 `src` 中的 `common` 文件夹中的 `web.json` 文件换成你自己的版本


### 设置 json 格式

>文件位置/src/common/web.json

```js
[
  {
    "title": "实用网站", //分类名字
    "children": [
      {
        "text": "网站一", //网站名字(必须)
        "url": "https://www.xxx.com/",//网站链接(必须)
        "icon": "https://www.xxx/com/logo.png", //图标 如果自动获取不到的话可手动填入(可选)
        "desc": "网站描述" //鼠标停留的描述 (可选)
      },
      {
        "text": "网站二", 
        "url": "https://www.xxx.com/",
        "icon": "https://www.xxx/com/logo.png", 
        "desc": "网站描述" 
      },
    ]
  },
    {
    "title": "有趣网站",//分类二
    "children": [
      {
        "text": "网站一", 
        "url": "https://www.xxx.com/",
        "icon": "https://www.xxx/com/logo.png", 
        "desc": "网站描述" 
      },
      {
        "text": "网站二", 
        "url": "https://www.xxx.com/",
        "icon": "https://www.xxx/com/logo.png", 
        "desc": "网站描述" 
      },
    ]
  },
]
```
## 个性化

### 更换主题颜色

>文件位置/src/assets/css/okarin.less

将第一行的主题颜色改为你喜欢的颜色

```less
 @theme-color: #007acc;
```

### 去除诗词

>文件位置/src/App.vue

如果你不喜欢头部的诗句，可以删除上面的文件，同时修改下面代码

```js
   <poem/> //删除
   import Poem from './Poem.vue' //删除
   components: {WebSet,Poem,BackToTop}, => components: { WebSet,BackToTop}, //修改
```

### 标题和描述

>文件位置/public/index.html

修改标题和描述

```html
<title>膻味书屋</title>
<meta name=description content="偶像练习生的各种网页收藏"> 
```
### 页脚

>文件位置/src/App.vue

不建议修改页脚，如果你一定要修改的话，更改如下文件

```html
<div class="footer">
      MIT Licensed | Copyright © 2022-present  <a href="https://github.com/Okarin1/web-project" target="_blank">@Okarin</a>
</div>
```

## 部署

本页面目前部署在[vercel](https://vercel.com/)

将修改后的项目，新建一个仓库并连接vercel自动打包部署，更多教程请自行搜索


