---
title: Hexo博客主题之hexo-theme-matery的介绍
date: 2018-09-28 13:34:00
author: blinkfox
top: true
categories: 前端
tags:
  - Hexo
---

[English Document](README.md) | [演示示例](https://blinkfox.github.io/) | QQ交流群:`926552981`

> 这是一个采用`Material Design`和响应式设计的 Hexo 博客主题。

## 特性

- 简单漂亮，文章内容美观易读
- [Material Design](https://material.io/)设计
- 响应式设计，博客在桌面端、平板、手机等设备上均能很好的展现
- 每天动态切换`Banner`图片
- 瀑布流式的博客文章列表(文章无特色图片时会有`24`张漂亮的图片代替)
- 时间轴式的归档页
- **词云**的标签页和**雷达图**的分类页
- 丰富的关于我页面（包括关于我、文章统计图、我的项目、我的技能、相册等）
- 可自定义的数据的友情链接页面
- 支持文章置顶和文章打赏
- 支持`MathJax`
- `TOC`目录
- 可设置复制文章内容时追加版权信息
- 可设置阅读文章时做密码验证
- [Gitalk](https://gitalk.github.io/)、[Gitment](https://imsun.github.io/gitment/)、[Valine](https://valine.js.org/)和[Disqus](https://disqus.com/)评论模块（推荐使用`Gitalk`）
- 集成了谷歌分析(`Google Analytics`)

## 后续开发计划

- [x] 重构标签页为**可分页**
- [x] 重构归档页为**可分页**
- [x] 增加分类页
- [x] 增加关于我页面
- [x] 阅读文章验证密码
- [x] 集成[Gitalk](https://gitalk.github.io/)
- [x] 右上角实现`fork me on github`
- [x] 添加`RSS`
- [x] 添加文章`TOC`
- ~~网站底部加上访问量等统计功能~~（主题使用者可以基于谷歌分析、百度统计、LeanCloud等来实现）
- [x] 首页设计和添加置顶文章
- [x] 文章结束后增加**打赏**功能
- ~~为博客添加萌萌的**宠物**或者**成长树**等~~（可以使用[hexo-helper-live2d](https://github.com/EYHN/hexo-helper-live2d)插件来实现）
- [x] 集成[Valine](https://valine.js.org/)
- [x] 增加阅读文章验证密码的功能
- [x] 增加了对`MathJax`的支持
- [ ] 制作一个LOGO
- [x] 增加友情链接页面
- [x] 添加复制文章内容时追加博客版权信息

> 欢迎贡献!

## 下载

当你看到这里的时候，应该已经有一个自己的[Hexo](https://hexo.io/zh-cn/)博客了，如果还没有的话，不妨使用 Hexo 和[Markdown](https://www.appinn.com/markdown/)来写博客和文章。

点击 [这里](https://codeload.github.com/blinkfox/hexo-theme-matery/zip/master) 下载`master`分支的最新稳定版的代码，解压缩后，将`hexo-theme-matery`的文件夹复制到你 Hexo 的`themes`文件夹中即可。当然你也可以在你的`themes`文件夹下使用`Git clone`命令来下载:

```bash
git clone https://github.com/blinkfox/hexo-theme-matery.git
```

## 配置

### 切换主题

修改 Hexo 根目录下的`_config.yml`的`theme`的值：`theme: hexo-theme-matery`

#### `_config.yml`文件的其它修改建议

- 请修改`_config.yml`的`url`的值为你的网站主`URL`（如：`http://xxx.github.io`）。
- 建议修改两个`per_page`的分页条数值为`6`的倍数，如：`12`、`18`等，这样文章列表在各个屏幕下都能较好的显示。
- 如果你是中文用户，则建议修改`language`的值为`zh-CN`。

### 新建分类 categories 页

`categories`页是用来展示所有分类的页面，如果在你的博客`source`目录下还没有`categories/index.md`文件，那么你就需要新建一个，命令如下：

```bash
hexo new page "categories"
```

编辑你刚刚新建的页面文件`/source/categories/index.md`，至少需要以下内容：

```yaml
---
title: categories
date: 2018-09-30 17:25:30
type: "categories"
layout: "categories"
---
```

### 新建标签 tags 页

`tags`页是用来展示所有标签的页面，如果在你的博客`source`目录下还没有`tags/index.md`文件，那么你就需要新建一个，命令如下：

```bash
hexo new page "tags"
```

编辑你刚刚新建的页面文件`/source/tags/index.md`，至少需要以下内容：

```yaml
---
title: tags
date: 2018-09-30 18:23:38
type: "tags"
layout: "tags"
---
```

### 新建关于我 about 页

`about`页是用来展示**关于我和我的博客**信息的页面，如果在你的博客`source`目录下还没有`about/index.md`文件，那么你就需要新建一个，命令如下：

```bash
hexo new page "about"
```

编辑你刚刚新建的页面文件`/source/about/index.md`，至少需要以下内容：

```yaml
---
title: about
date: 2018-09-30 17:25:30
type: "about"
layout: "about"
---
```

### 新建友情连接 friends 页（可选的）

`friends`页是用来展示**友情连接**信息的页面，如果在你的博客`source`目录下还没有`friends/index.md`文件，那么你就需要新建一个，命令如下：

```bash
hexo new page "friends"
```

编辑你刚刚新建的页面文件`/source/friends/index.md`，至少需要以下内容：

```yaml
---
title: friends
date: 2018-12-12 21:25:30
type: "friends"
layout: "friends"
---
```

同时，在你的博客`source`目录下新建`_data`目录，在`_data`目录中新建`friends.json`文件，文件内容如下所示：

```json
[{
    "avatar": "http://image.luokangyuan.com/1_qq_27922023.jpg",
    "name": "码酱",
    "introduction": "我不是大佬，只是在追寻大佬的脚步",
    "url": "http://luokangyuan.com/",
    "title": "前去学习"
}, {
    "avatar": "http://image.luokangyuan.com/4027734.jpeg",
    "name": "闪烁之狐",
    "introduction": "编程界大佬，技术牛，人还特别好，不懂的都可以请教大佬",
    "url": "https://blinkfox.github.io/",
    "title": "前去学习"
}, {
    "avatar": "http://image.luokangyuan.com/avatar.jpg",
    "name": "ja_rome",
    "introduction": "平凡的脚步也可以走出伟大的行程",
    "url": "ttps://me.csdn.net/jlh912008548",
    "title": "前去学习"
}]
```

### 代码高亮

由于 Hexo 自带的代码高亮主题显示不好看，所以主题中使用到了[hexo-prism-plugin](https://github.com/ele828/hexo-prism-plugin)的 Hexo 插件来做代码高亮，安装命令如下：

```bash
npm i -S hexo-prism-plugin
```

然后，修改 Hexo 根目录下`_config.yml`文件中`highlight.enable`的值为`false`，并新增`prism`插件相关的配置，主要配置如下：

```yaml
highlight:
  enable: false

prism_plugin:
  mode: 'preprocess'    # realtime/preprocess
  theme: 'tomorrow'
  line_number: false    # default false
  custom_css:
```

### 搜索

本主题中还使用到了[hexo-generator-search](https://github.com/wzpan/hexo-generator-search)的 Hexo 插件来做内容搜索，安装命令如下：

```bash
npm install hexo-generator-search --save
```

在 Hexo 根目录下的`_config.yml`文件中，新增以下的配置项：

```yaml
search:
  path: search.xml
  field: post
```

### 中文链接转拼音（可选的）

如果你的文章名称是中文的，那么 Hexo 默认生成的永久链接也会有中文，这样不利于`SEO`，且`gitment`评论对中文链接也不支持。我们可以用[hexo-permalink-pinyin](https://github.com/viko16/hexo-permalink-pinyin) Hexo 插件使在生成文章时生成中文拼音的永久链接。

安装命令如下：

```bash
npm i hexo-permalink-pinyin --save
```

在 Hexo 根目录下的`_config.yml`文件中，新增以下的配置项：

```yaml
permalink_pinyin:
  enable: true
  separator: '-' # default: '-'
```

> **注**：除了此插件外，[hexo-abbrlink](https://github.com/rozbo/hexo-abbrlink)插件也可以生成非中文的链接。

### 添加RSS订阅支持（可选的）

本主题中还使用到了[hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)的 Hexo 插件来做`RSS`，安装命令如下：

```bash
npm install hexo-generator-feed --save
```

在 Hexo 根目录下的`_config.yml`文件中，新增以下的配置项：

```yaml
feed:
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
  content_limit: 140
  content_limit_delim: ' '
  order_by: -date
```

执行 `hexo clean && hexo g`重新生成博客文件，然后在`public`文件夹中即可看到`atom.xml`文件，说明你已经安装成功了。

### 修改社交链接

在主题文件的`/layout/_partial/social-link.ejs`文件中，你可以修改或添加你需要的社交链接地址，增加链接可参考如下代码：

```html
<a href="https://github.com/blinkfox" class="tooltipped" target="_blank" data-tooltip="访问我的GitHub" data-position="top" data-delay="50">
    <i class="fa fa-github"></i>
</a>
```

其中，社交图标（如：`fa-github`）你可以在[Font Awesome](https://fontawesome.com/icons)中搜索找到。以下是常用社交图标的标识，供你参考：

- Facebook: `fa-facebook`
- Twitter: `fa-twitter`
- Google-plus: `fa-google-plus`
- Linkedin: `fa-linkedin`
- Tumblr: `fa-tumblr`
- Medium: `fa-medium`
- Slack: `fa-slack`
- 新浪微博: `fa-weibo`
- 微信: `fa-wechat`
- QQ: `fa-qq`

> **注意**: 本主题中使用的`Font Awesome`版本为`4.5.0`。

### 修改打赏的二维码图片

在主题文件的`source/medias/reward`文件中，你可以替换成你的的微信和支付宝的打赏二维码图片。

## 文章Front-matter示例

以下为文章`Front-matter`的示例，所有内容均为**非必填**的。但是，仍然建议至少填写`title`的值，当然最好都填写上这些文章信息。

```yaml
---
title: typora-vue-theme主题介绍
date: 2018-09-07 09:25:00
author: 赵奇
img: /source/images/xxx.jpg # 或者:http://xxx.com/xxx.jpg
top: true # 如果top值为true，则会是首页推荐文章
# 如果要对文章设置阅读验证密码的话，就可以在设置password的值，该值必须是用SHA256加密后的密码，防止被他人识破
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
# 本文章是否开启mathjax，且需要在主题的_config.yml文件中也需要开启才行
mathjax: false
categories: Markdown
tags:
  - Typora
  - Markdown
---
```

> **注意**:
> 1. 如果`img`属性不填写的话，文章特色图会根据文章标题的`hashcode`的值取余，然后选取主题中对应的特色图片，从而达到让所有文章都的特色图**各有特色**。
> 2. `date`的值尽量保证每篇文章是唯一的，因为本主题中`Gitalk`和`Gitment`识别`id`是通过`date`的值来作为唯一标识的。
> 3. 如果要对文章设置阅读验证密码的功能，不仅要在Front-matter中设置采用了SHA256加密的password的值，还需要在主题的`_config.yml`中激活了配置。有些在线的 SHA256 加密的地址，可供你使用：[开源中国在线工具](http://tool.oschina.net/encrypt?type=2)、[chahuo](http://encode.chahuo.com/)、[站长工具](http://tool.chinaz.com/tools/hash.aspx)。

## 效果截图

![首页](http://static.blinkfox.com/matery-20181202-1.png)

![首页推荐文章](http://static.blinkfox.com/matery-20181202-2.png)

![首页文章列表](http://static.blinkfox.com/matery-20181202-3.png)

![首页文章列表](http://static.blinkfox.com/matery-20181202-7.png)

![首页文章列表](http://static.blinkfox.com/matery-20181202-8.png)

## 自定制修改

在本主题的`_config.yml`中可以修改部分自定义信息，有以下几个部分：

- 菜单
- 首页的励志名言
- 是否显示推荐文章名称和按钮配置
- `favicon` 和 `Logo`
- 个人信息
- TOC目录
- 文章打赏信息
- 复制文章内容时追加版权信息
- MathJax
- 我的项目
- 我的技能
- 我的相册
- `Gitalk`、`Gitment`、`Valine`和`disqus`评论配置
- 谷歌分析(`Google Analytics`)
- 默认特色图的集合。当文章没有设置特色图时，本主题会根据文章标题的`hashcode`值取余，来选择展示对应的特色图

**我认为个人博客应该都有自己的风格和特色**。如果本主题中的诸多功能和主题色彩你不满意，可以在主题中自定义修改，很多更自由的功能和细节点的修改难以在主题的`_config.yml`中完成，需要修改源代码才来完成。以下列出了可能对你有用的地方：

### 修改主题颜色

在主题文件的`/source/css/matery.css`文件中，搜索`.bg-color`来修改背景颜色：

```css
/* 整体背景颜色，包括导航、移动端的导航、页尾、标签页等的背景颜色. */
.bg-color {
    background-image: linear-gradient(to right, #4cbf30 0%, #0f9d58 100%);
}

/* 和背景颜色相同的文字颜色，目前仅在首页一个地方使用到，你也可以将此样式应用到其他地方. */
.text-color {
    color: #0f9d58 !important;
}

@-webkit-keyframes rainbow {
   /* 动态切换背景颜色. */
}

@keyframes rainbow {
    /* 动态切换背景颜色. */
}
```

### 修改banner图和文章特色图

你可以直接在`/source/medias/banner`文件夹中更换你喜欢的`banner`图片，主题代码中是每天动态切换一张，只需`7`张即可。如果你会`JavaScript`代码，可以修改成你自己喜欢切换逻辑，如：随机切换等，`banner`切换的代码位置在`/layout/_partial/bg-cover.ejs`文件的`<script></script>`代码中：

```javascript
$('.bg-cover').css('background-image', 'url(/medias/banner/' + new Date().getDay() + '.jpg)');
```

在`/source/medias/featureimages`文件夹中默认有24张特色图片，你可以再增加或者减少，并需要在`_config.yml`做同步修改。
