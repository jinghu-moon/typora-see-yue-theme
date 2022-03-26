## 1.1 主题使用

1. 下载右侧的 release 包。
2. 解压后的文件直接放入 Typora 的 themes 文件夹。
3. 重启 Typora，主题选择 See Yue，开始愉快地写作！

下载失败，请点击这个链接： 

## 1.2 主题介绍

See Yue 主题是一个自定义样式极多、简约、但处处充满细节的 Typora **明亮**主题。

See Yue 主题针对**中文**做了优化。

See Yue 主题以  [vue](https://github.com/blinkfox/typora-vue-theme) 主题为框架，参考了网上诸多的教程和 Typora 主题，才制作出来。非常感谢他们的无私分享！

### 1.2.1 设计思路

**1、字体**

我将 Typora 整个界面分为两部分：写作区、侧边栏

- 写作区分为正文、目录、标题。
  - 正文使用 Lora ＋ [汉仪玄宋 45S](https://www.hanyi.com.cn/productdetail?id=8216) 。
  - 正文目录使用 RobotoMono（等宽字体）＋ 汉仪玄宋 45S。
  - 标题使用 [HarmonyOS](https://developer.harmonyos.com/cn/docs/design/font-0000001157868583) 。
- 侧边栏和底部栏统一使用 RobotoMono ＋ [霞鹜文楷](https://www.maoken.com/freefonts/9704.html) 。
- 正文的字号（20px）相较于其他主题，大了不少。是因为宋体的字号不够大的话，看起来会很难看。相应的，标题的字号也很大。

个人认为宋体和楷体的搭配，还是挺不错的。

**2、色彩**

See Yue 主题在色彩的选用上比较克制，主要使用绿色、蓝色、橙色。

- 绿色用于标题、列表符号，给人一种比较柔和的感觉。
- 侧边栏底色为浅浅蓝色、强调色为暗蓝色，并以白色作为底色。正文中的引用块底色为浅浅蓝色。
- 在一级标题、标题等级提示、行内代码、表格首行使用橙色，与其他的内容形成对比。

- 对于链接，显示为绿色。当鼠标悬浮其上时，颜色变为橙色。

**3、整体界面**

个人比较喜欢圆润的风格，看起来比较舒服。

- 侧边栏圆角化，并增加阴影。
- 凡是在正文部分的内容底色统一圆角化。
- 表格、图片圆角化。
- 鼠标滚轮圆角化。

圆角大法好！ 🤣

### 1.2.2 注意

- See Yue 主题是我学习 CSS 的练手之作，代码风格可能极其不规范。不过大部分代码，我都写了注释，应该还是比较好理解的。
- 本主题仅在 Windows 上做过测试，不保证在 Mac 上可以达到同样效果。如果在 Mac 上出现了问题，请尽量自行修复。本人没有 Mac 电脑，无法做测试。抱歉。

## 1.3 主题文件

### 1.3.1 资源文件

下面是一些主题使用到的资源文件。

| 文件夹        | 用途               |
| ------------- | ------------------ |
| Chinese_fonts | 中文字体           |
| English_fonts | 英文字体           |
| lcon          | 部分网站 logo      |
| lcon_font     | 主题使用的图标     |
| Picture       | 毛玻璃效果的背景图 |

### 1.3.2 CSS 文件

由于主题功能多，代码量也比较大，为便于使用者修改，我将代码分割成不同的 CSS 文件，每一份 CSS 文件都有着独立且不同的功能。下面是主题的 CSS 文件及其用途。

 `2` 到 `12` 的 CSS 文件，为功能实现文件，已在 `see-yue.css` 引入。 `13` 到 `14` 的 CSS 文件，为参考文件，可作为样式修改参考。

| 序号 | 文件                 | 用途                             | 备注                             |
| :--: | :------------------- | -------------------------------- | -------------------------------- |
|  1   | `see-yue.css`        | 主题主体部分                     | 无                               |
|  2   | `auto-number.css`    | 大纲、正文目录、正文标题自动编号 | 可选                             |
|  3   | `code-block.css`     | 代码块样式设置                   | **必选**                         |
|  4   | `code-language.css`  | 代码块显示编程语言。             | 可选                             |
|  5   | `code-snippet.css`   | 零散的样式修改                   | **必选**                         |
|  6   | `contents.css`       | 正文目录样式设置                 | 可选                             |
|  7   | `fonts.css`          | 字体引用                         | **必选**                         |
|  8   | `frosted-glass.css`  | 毛玻璃效果，                     | 可选。雏形，不建议使用。         |
|  9   | `headline.css`       | 标题样式设置                     | **必选**                         |
|  10  | `sidebar.css`        | 侧边栏设置                       | **必选**                         |
|  11  | `to-pdf.css`         | 导出 PDF 设置                    | **必选**                         |
|  12  | `website-icon.css`   | 显示部分网站 logo                | 可选                             |
|  13  | `nord.css`           | 代码块配色                       | 作参考，未使用。                 |
|  14  | `root-attribute.css` | 根属性                           | 作参考，未使用 |

我的选择如下：

![01-配置](https://s3.bmp.ovh/imgs/2022/03/9045053c4db552fb.png)

## 1.4 主题功能

### 1.4.1 标题等级提示

如下：

![02-等级提示](https://s3.bmp.ovh/imgs/2022/03/f49fa1736e2a1f0e.png)

相关代码在 `headline.css` 末尾。

### 1.4.2 自动编号

侧边栏、正文目录、正文标题自动编号。

<span style="color:#b91919;font-weight:bolder">注意：</span>启用此功能，需要注释『标题等级提醒』的相应代码。

```css
/* headline.css */
/* ————————————————————————————————————标题等级提示———————————————————————————————————*/
/* 注释掉以下所有代码 */
```

如果你觉得二级标题编号在背景外面，不好看，可以修改代码。

打开 `headline.css` ，修改如下：

```css
/* 以下代码覆盖原来的二级标题样式一 */
#write h2  {
    display: inline-block;
    font-weight: bold;
    /* background: #e07a5f; */
    color: #ffffff;
    padding: 0px 6px 0px;
    border-radius: 4px;
    background-image: linear-gradient(to bottom, #74c69d, #b7e4c7);
}

#write h2:after {
    display: inline-block;
    content: "";
    position: absolute;
    bottom: -10px;
    top: auto;
    background-image: linear-gradient(to right, #c1dfc4 0%, #deecdd 100%);
    left: 0;
    right: 0;
    height: 4px;
    width: 940px;
}

/* 取消以下代码的注释*/
#write h2,
#write h2::before {
    color: #fff !important;
    font-family: "HarmonyOS";
}
```

<span style="color:#b91919;font-weight:bolder">注意：</span>修改后，会出现问题，两个二级标题中间没有文字、空格时，它们会合并到一行上去。如果有文字、则不会合并。

> 此代码来自于 [@萌佬](https://github.com/Zuoqiu-Yingyi) 的思源笔记主题 [Zuoqiu-Yingyi/siyuan-theme-dark-plus: 思源笔记的一款暗黑主题(A dark theme of SiYuan Note) (github.com)](https://github.com/Zuoqiu-Yingyi/siyuan-theme-dark-plus) 。我只做了简单修改。感谢萌佬！

### 1.4.3 代码块显示编程语言

代码块会自动在右上角显示你选择的编程语言。如果没有显示，有两种可能。

1. 选择代码块语言时，是自己输入的字符，不能被识别。建议在输入框选择自己的代码语言。

2. CSS 文件没有添加该编程语言。可以在 `code-language.css` 添加相应代码。

   添加方式如下：

   ````css
   pre[lang$='xxx']:before {
       content: 'xxx';
   }
   /* xxx 为你填写的编程语言 */
   ````

PS：我已经将输入框显示的所有编程语言写入了 CSS 文件。应该不会存在第二种情况。

### 1.4.4 网络图片标识

对于上传至图床（网络）的图片，会在右上角显示一个云朵图标。如下：

![灰绿](https://s3.bmp.ovh/imgs/2022/03/7efab3a023690589.webp)

此代码还可以优化。比如根据上传平台的不同，显示对应的网站 logo 。有需要的朋友可以自行修改。

导出 PDF 不会显示该图标，正合我意。😉

<span style="color:#b91919;font-weight:bolder">缺陷：</span>图标不能随图片大小改变而改变位置。🙃

### 1.4.5 图片错误显示

如下：

![测试](https://s3.bmp.ovh/imgs/2022/03/f58a8248042b82d0.png)

### 1.4.6 链接图标

此功能默认关闭。

链接默认末尾增加一个小链接图标，部分网站链接首端有对应网站 logo 。

如果你的链接没有对应 logo 。可以在 `website-icon.css` 添加相应代码。

添加方式：

```css
a[href*="xxx.com"]::before {
    content: "";
    background-image: url("ico/xxx.svg");
}
/* 推荐使用 svg 格式图片，比较清晰。 */
```

[总结:如何获取网站的 favicon · 语雀 (yuque.com)](https://www.yuque.com/achuan-2/blog/rp2myq) （**补充**：源代码模式下还可以搜索 png、jpg、svg）

### 1.4.7 侧边栏大纲线

一级标题到五级标题，默认全部开启。相关代码在 `sidebar.css` 中。如下：

![03-大纲线](https://s3.bmp.ovh/imgs/2022/03/831ad21f539d22c6.png)

同时，将侧边栏默认的折叠、展开图标换成更明显的三角：▶、▼（我比较喜欢）。

### 1.4.8 正文目录设置

正文生成的目录添加左边框（透明），增加可点击范围（**注意：**标题不能过长）。同时在目录上方增加 `“目录”` 二字。

相关代码在 `content.css` 。

### 1.4.9 列表设置

将列表符号颜色改为绿色，同时光标所在列表行的列表符号变为红色。无序列表增加层级线条。

如下：

![04-列表](https://s3.bmp.ovh/imgs/2022/03/8e0bef430e875881.png)

如何修改列表符号，请看 [list-style - CSS（层叠样式表） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/list-style) 。

### 1.4.10 引用样式块

相关代码在 `see-yue.css` 里 233 到 320 行。

不建议增加新的引用样式块，因为 H3 到 H6 的代码我都写好了。如果用 H1、H2，会与现有的标题样式冲突。建议修改已有的引用样式块代码。

使用方法：

```markdown
> ### Warning / 注意
>
> 这是一个三级标题。

> #### Quote / 参考
>
> 这是一个四级标题。

> ##### Tips / 提示
>
> 这是一个五级标题。

> ###### Expand / 拓展
>
> 这是一个六级标题。
```

示例如下：

> ### Warning / 注意
>
> 可用于警告读者不能做什么、必须做什么、这样做造成的后果。

> #### Quote / 参考
>
> 文章过长时，如果把参考的文章、视频放在末尾，会影响阅读体验。可使用该样式块。

> ##### Tips / 提示
>
> 提示读者可以怎么做，仅为建议。也可作为某段内容的注解。

> ###### Expand / 拓展
>
> 当你写的内容与本文关系不大或者属于进阶部分时，可使用该样式块。

### 1.4.11 summary 折叠标签

Typora 没有折叠文字、代码的功能，但我们可以用 `summary` 标签实现。

使用方法如下：

<details>
    <summary>折叠标签</summary>
    <ol><li> 测试一下吧！</li></ol><ul><li> 测试一下吧！</li></ul>
    <p>海客谈瀛洲，烟涛微茫信难求，越人语天姥，云霞明灭或可睹。天姥连天向天横，势拔五岳掩赤城。天台一万八千丈，对此欲倒东南倾。</p>
    <blockquote>
        测试一下吧！
    </blockquote>
    <strong>镜湖月</strong> <u>镜湖月</u> <i>镜湖月</i> 
</details>

显示某种样式，需要使用对应的 HTML 标签。很麻烦。如果想内嵌代码块的话，就更麻烦。算是聊胜于无吧。希望官方可以支持**代码块折叠**。


## 1.5 参考主题

| 主题                                                         | 用途                         |
| ------------------------------------------------------------ | ---------------------------- |
| [blinkfox/typora-vue-theme](https://github.com/blinkfox/typora-vue-theme) | See Yue 主题框架             |
| [evgo2017/typora-theme-orange-heart](https://github.com/evgo2017/typora-theme-orange-heart) | 二级标题样式、脚注样式       |
| [HanryYu/typora-blubook-theme](https://github.com/HanryYu/typora-blubook-theme) | 标题等级提醒                 |
| [h16nning/typora-gitbook-theme](https://github.com/h16nning/typora-gitbook-theme) | 侧边栏选中样式               |
| [Soanguy/typora-theme-autumnus](https://github.com/Soanguy/typora-theme-autumnus) | 毛玻璃效果                   |
| [muggledy/typora-dyzj-theme](https://github.com/muggledy/typora-dyzj-theme) | 折叠标签                     |
| [li3zhen1/Fluent-Typora](https://github.com/li3zhen1/Fluent-Typora) | 引用样式块                   |
| [ChristosBouronikos/typora-nord-theme](https://github.com/ChristosBouronikos/typora-nord-theme) | 侧边栏阴影、表格阴影模拟边框 |

还有别的参考文章，由于时间久远，找不到了。非常抱歉。

再次感谢这些主题、文章的提供者。

## 1.6 主题 Bug

这么多的自定义样式、代码，出现 Bug 是在所难免的。 🙃

1、表格聚焦，边框消失

- **Bug** 

![05-表格bug](https://s3.bmp.ovh/imgs/2022/03/051ee0f317f9c413.gif)

- **复现**

  长文档（字数超过 2W 字），可以比较稳定复现。

- **后果**

  没有后果，就是动画显示的样子。不影响操作表格、导出 PDF。

- **解决**

  使用 border 属性，添加边框，应该可以解决。但是我不愿意。使用 border 添加的边框，再加边框圆角，样式极其难看。

**其余的 Bug 还没发现。**

如果你在使用主题的时候发现了一些用起来不舒服的地方，请提 `Issues` 或者自行解决。


## 1.7 结束语

我非常乐意，你在 See Yue 主题下，写一个自己的 Typora 主题。对于可能会修改的部分，我给了详细的注释。

**参考网站**： [CSS - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS) 、 [ HTML  - 学习 Web 开发 | MDN ](https://developer.mozilla.org/zh-CN/docs/Learn/HTML) 

**参考视频**： [【不吃鸡蛋黄啃编程】typora 自定义好看的背景 自己的配色方案 - bilibili](https://www.bilibili.com/video/BV1Lt4y1D7kN?from=search&seid=8687069285771528770&spm_id_from=333.337.0.0) 

此外，我还制作了两个简易封面模板。这样一来，笔记就有了封面。good！

封面模板 1 适合字数较少的笔记名，封面模板 2 适合字数较多的笔记名。

> ~~对我来说，美化没有尽头。~~目前，暂告一段落。
>
> See Yue 主题,个人认为已经很完善了。（在没有发现 Bug 之前）















































