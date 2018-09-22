# Material X


> 一个简约卡片式的Hexo博客主题

**Material X** 是我基于 [Material Flow](https://github.com/stkevintan/hexo-theme-material-flow)（已停止维护） 改编的一个Hexo主题，相对作者原主题主要有以下方面改动：

- 调整卡片阴影细节以及增加卡片的动画效果。
- 博文列表将作者的多列布局改为单列布局。
- 使用 [fontawesome](http://fontawesome.io) 图标。
- 优化了颜色搭配，方便在defines中更换主题色。
- 一些UI细节，如调整搜索框长度使之与右边卡片等宽、优化了在手机端的显示效果。
- 可以显示网易云音乐歌单。
- 支持3种评论系统：Disqus、来必力和Valine。
- 增加了推荐文章列表，增加博客流量。
- 增加了阅读统计。
- 支持渲染MathJax数学公式。
- 修复了目录有时无法定位的BUG。



## Demo

本主题将持续更新和维护，你可以在这里查看主题最新的实际效果：👉 [https://blog.xaoxuu.com](https://blog.xaoxuu.com) 👈

**以及其他使用 Material X 主题的博主：**

| 博客         | 链接                 |
| ------------ | -------------------- |
| MicDZ's blog | https://www.micdz.cn |
| 大涛子峡谷 | https://istaotao.com |

> 如果你使用了 **Material X** 主题，欢迎提PR到这里告诉大家~



## 安装

提供两种安装方式：脚本和手动，脚本不仅可以安装主题，还可以方便你发布博客，详见 [@hexo.sh](https://github.com/xaoxuu/hexo.sh) 。



### A. 脚本安装【推荐】

首先打开终端，`cd`到你博客的路径，如果你想省事，复制下面这行脚本到终端中执行，全程自动化操作。

```bash
curl -O 'https://raw.githubusercontent.com/xaoxuu/hexo.sh/master/hexo.sh' -# && chmod 777 hexo.sh && . hexo.sh -i i x
```

如果你选择了脚本安装，现在可以直接往下看配置项啦~



### B. 手动安装

如果你想手动安装，第一步下载主题到`themes/`文件夹：

```bash
git clone https://github.com/xaoxuu/hexo-theme-material-x themes/material-x
```

然后安装依赖包：

```bash
npm i -S hexo-generator-search hexo-generator-feed hexo-renderer-less hexo-autoprefixer hexo-generator-json-content hexo-recommended-posts
```



## 文档

https://xaoxuu.com/wiki/material-x



## 主题配置

把 `themes/material-x/_config.yml` 中的 **所有** 内容复制到博客主目录的 `_config.yml` 文件中，然后根据自己的需要填写和修改。这样做的好处是：更新主题的时候你修改过的配置就不会被覆盖了。

> 以下这些配置如果没有特殊说明，都指的是博客主目录的 `_config.yml` 文件。

### 导航栏

你可以找到类似这一段，把它改为你需要的：

```yaml
# 导航栏
nav_menu:
  - name: 主页
    slug: about
    icon: fa-home
    url: /
  - name: 项目
    slug: projects
    icon: fa-cube
    url: https://xaoxuu.com/proj
  - name: 博客
    slug: home
    icon: fa-rss
    url: /
  - name: 归档
    slug: archives
    icon: fa-archive
    url: /archives
```

其中 icon 是 `font-awesome` 图标名，你要显示什么图标，去 [font-awesome](https://fontawesome.com/icons?d=gallery) 找就可以了。



### 侧边栏

右边的小窗口，可以根据需要显示。

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  # 博主信息，显示个人头像、格言、社交信息等
  author:
    enable: true
    avatar: https://xaoxuu.com/assets/img/avatar.jpg # 头像，如果config中已经设置avatar了，这里可以不用写
    title: 某知名博主 # 博客名、头衔等等，居中显示
    motto: 某知名博主的座右铭啊哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈。 # 格言座右铭等等
    social: true # 是否显示社交信息（内容同页脚的社交信息）
  # 显示文章分类
  categories: true
  # 显示文章标签
  tagcloud: true
  # 显示网易云歌单
  musicid: 746319661 # 歌单id
  # 显示友链
  links:
  - name: xaoxuu
    url: https://xaoxuu.com
  # 显示目录（在文章中设置toc:false可以隐藏单篇文章的目录）
  toc: true		
```



#### 博主（头像/头衔/格言/社交信息）

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  # 博主信息，显示个人头像、格言、社交信息等
  author:
    enable: true
    avatar: https://xaoxuu.com/assets/img/avatar.jpg # 头像，如果config中已经设置avatar了，这里可以不用写
    title: 某知名博主 # 博客名、头衔等等，居中显示
    motto: 某知名博主的座右铭啊哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈。 # 格言座右铭等等
    social: true # 是否显示社交信息（内容同页脚的社交信息）
```


#### 分类

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  ...
  # 显示文章分类
  categories: true
```



#### 标签

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  ...
  # 显示文章标签
  tagcloud: true
```



#### 网易云音乐歌单

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  ...
  # 显示网易云歌单
  musicid: 746319661 # 歌单id
```



#### 友链

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  ...
  # 显示友链
  links:
  - name: xaoxuu
    url: https://xaoxuu.com
```



#### 显示目录（TOC）

```yaml
# 右边的小窗口，不想显示哪一项的注释掉对应的即可
widgets:
  ...
  # 显示目录（在文章中设置toc:false可以隐藏单篇文章的目录）
  toc: true		
```



### 推荐文章

如果你不想显示推荐文章，可以卸载 `hexo-recommended-posts` 这个依赖包。

```yaml
# 推荐文章
recommended_posts:
  autoDisplay: false # 自动在文章底部显示推荐文章，如果你使用Material-X主题，这里要设置为false。
  server: https://api.truelaurel.com # 后端推荐服务器地址
  timeoutInMillis: 10000 # 服务时长，超过此时长，则使用离线推荐模式
  excludePattern: []
  titleHtml: <h4>推荐文章</h4> #自定义标题
  internalLinks: 3 # 内部文章数量
  externalLinks: 2 # 外部文章数量
  fixedNumber: false
```

> 注意：autoDisplay: false 这一项不要修改，因为自动显示效果不佳，我已经在主题里给它设置显示位置了。



### 评论

提供3种可选，如果你使用其他的评论系统，请自己修改主题。

#### Disqus

官网： [http://disqus.com/](http://disqus.com/)

```yaml
# disqus评论
disqus_shortname: #你的disqus的shortname#
```

#### Livere 来必力

官网： [http://www.laibili.com.cn/](http://www.laibili.com.cn/)

```yaml
# 来必力评论
livere_shortname: #你的disqus的shortname#
```
#### Valine

官网： [https://valine.js.org](https://valine.js.org)

```yaml
# valine
valine:
  enable: true # 如果你想用Valine评论系统，请设置enable为true
  appId:  # 必填
  appKey:  # 必填
  guest_info: nick,mail,link #valine comment header info
  placeholder: 快来评论吧~ # valine comment input placeholder(like: Please leave your footprints )
  avatar: mp # gravatar style https://valine.js.org/avatar
  pageSize: 10 # comment list page size
  verify: false # valine verify code (true/false)
  notify: false # valine mail notify (true/false)
  lang: zh-cn
```



### 页脚

```yaml
# 页脚社交信息
social:
  - icon: fa-envelope
    url: mailto:me@xaoxuu.com
  - icon: fa-github
    url: https://github.com/xaoxuu
  - icon: fa-instagram
    url: https://www.instagram.com/xaoxuu
  - icon: fa-google-plus
    url:
  - icon: fa-twitter
    url: https://twitter.com/xaoxuu
  - icon: fa-music
    url: https://music.163.com/#/user/home?id=63035382
  - icon: fa-rss
    url: atom
  - icon: fa-telegram
    url:
  - icon: fa-vimeo
    url:
  - icon: fa-gitlab
    url:
  - icon: fa-linkedin
    url:
  - icon: fa-snapchat
    url:
  - icon: fa-steam
    url:
  - icon: fa-spotify
    url:
  - icon: fa-tumblr
    url:
  - icon: fa-youtube
    url:
  - icon: fa-weibo
    url:
  - icon: fa-weixin
    url:
  - icon: fa-qq
    url:
```





## 单篇文章的配置

### 某一篇文章不想开启评论

```
---
comments: false
---
```

### 某一篇文章不想在底部显示推荐文章

```
---
recommended_posts: false
---
```

### 开启渲染MathJax数学公式

```
---
mathjax: true
---
```



## 样式自定义

找到 `themes/material-x/source/less/_defines.less` 这个文件。

> 由于这个文件在 `themes/material-x` 中，所以更新主题的时候先备份一下 `_defines.less` 这个文件，更新之后对比改动自行修改。



### 字体

调整这些字体的顺序：

```yaml
// 大部分文字字体
@fontfamily_base: 'Ubuntu', Menlo, Monaco, Helvetica, "Hiragino Sans GB", "Hiragino Sans GB W3", Source Han Sans CN Regular, WenQuanYi Micro Hei, "Microsoft YaHei", Arial, sans-serif;
// 代码字体
@fontfamily_code: Menlo, Monaco, @fontfamily_base;
// LOGO字体
@fontfamily_logo: @fontfamily_base;
```

默认的字体 `Ubuntu` 使用的是GoogleFontsAPI：

```html
<link href="https://fonts.googleapis.com/css?family=Ubuntu" rel="stylesheet">
```

你想使用其他字体，可以自己去 [https://fonts.google.com](https://fonts.google.com/) 找，然后将代码添加到 `themes/material-x/layout/_partial/head.ejs` 中，然后把字体名添加到 `@xxx-font-family` 第一位。



### 字号

```yaml
// base
@fontsize_base:   16px;
@fontsize_small:  @fontsize_base * 0.875;
@lineheight_base: 1.7;
// title
@fontsize_h1: @fontsize_base * 1.5;
@fontsize_h2: @fontsize_base * 1.4;
@fontsize_h3: @fontsize_base * 1.2;
@fontsize_h4: @fontsize_base * 1.1;
@fontsize_h5: @fontsize_base * 1;
@fontsize_h6: @fontsize_small;
// article
@fontsize_article_title: @fontsize_h1 * 1.2;
@fontsize_article_title_phone: @fontsize_h2;
```



### 布局尺寸

```yaml
@on_modal_threshold:  680px;
@on_phone:         820px;
@on_laptop:        990px;
@on_desktop:       1200px;
// container
@width_container:  1200px;
// post
@width_post_max: 980px;
// 侧边栏宽度
@width_sidebar: 250px;
// 搜索框的宽度，建议和侧边栏宽度保持一致
@width_searchbar: @width_sidebar;
// 一个cell的高度
@height_cell: 36px;
```



### 导航栏

```yaml
// 导航栏高度
@height_navbar: 54px;
@fontsize_logo: 1.3em;
@fontsize_header_switcher: 1.3em;
@fontsize_header: 1em;
```



### 间距

目前很多地方的间距都是依据这个值：

```yaml
@gap: 20px;
```



### 圆角

```yaml
// 0px: 极端，2px：硬朗，4px：常规，8px：圆润，16px：温柔
@border_radius: 8px; // 圆角半径，可以根据心情随时调整风格
@border_radius_left_line: 4px; // 左边的竖线的宽度
@border_radius_code_block: 4px; // 代码块的圆角及其滚动条的宽度
```



### 配色

```yaml
// 背景色 ----------------
// 网页背景
@theme_bg_main: @theme_base_main;
// 导航栏背景
@theme_bg_navbar: darken(@theme_base_main, 4%);
// 卡片背景
@theme_bg_card: white;
// 卡片标题栏背景
@theme_bg_card_header: @theme_bg_navbar;
// 代码的背景色
@theme_bg_code: fade(@color_mac_maximize, 6%);
// 代码块的背景色
@theme_bg_code_block: @theme_bg_code;
// 引用的颜色以及分类、归档的 hover 时颜色
@theme_bg_quote: @theme_base_tint;
// 文字颜色 ----------------
// 标题文字颜色（h1/h2）
@theme_text_header: @theme_base_tint;
// 链接颜色
@theme_text_link: @color_ax_blue;
// 链接高亮颜色
@theme_text_highlight: @theme_base_tint;
// 在主题色中显示的文本（一般为白或深灰）
@theme_text_in_header: @dark;
// 正文文字颜色
@theme_text_main: @dark;
```

对应的效果如图所示：

![](https://img.vim-cn.com/70/5620af391b12439452a1e03413574fb3a1208c.png )



### 阴影

```yaml
// 卡片正常状态的阴影
@boxshadow_card_normal: @boxshadow_base_1, @boxshadow_base_2;
// 卡片漂浮起来时的阴影
@boxshadow_card_raised: @boxshadow_base_2, @boxshadow_base_4, @boxshadow_base_8, @boxshadow_base_16;
```



## 单元测试

如果你发现无法使用或者效果与 [示例](https://blog.xaoxuu.com) 有较大区别，可以使用hexo官方提供的用于单元测试的博客应用本主题查看样式。hexo.sh 脚本提供了方便的指令，详情见 hexo.sh 的 [文档](https://xaoxuu.com/wiki/hexo.sh)  。

如果你的电脑是不是mac，则无法使用脚本，可以手动下载单元测试博客： [https://github.com/hexojs/hexo-theme-unit-test.git](https://github.com/hexojs/hexo-theme-unit-test.git)，然后下载并应用本主题，查看效果。


其他的暂时不想写了，自己摸索吧~
