# emmet plus 让emmet更强大

## 如何使用？

以 Sublime Text 为例

1. 首先你得有个 emmet。
2. 打开 Sublime Text 的安装目录。
3. 在 Data 文件夹下面新建一个名为 emmet 的目录。
4. 拷贝`snippets-emmet-plus.json`到该目录下。
5. 打开 emmet 的配置文件`Emmet.sublime-settings`。
6. 修改`extensions_path` 后面的路径为之前新建的 emmet 目录的绝对路径，例如`D:/Program Files/Sublime Text 2.0.2/Data/emmet`。

尽情享受吧！

## 扩展了哪些功能？

* 统一的注释风格，以[css-creating](https://github.com/yisibl/css-creating)为参考。

例如输入`c`，`cc`

在HTMl文件中会输出：

```
<!--  -->

<!-- 模块名 begin -->
    
<!-- 模块名 end -->

```

在 CSS 文件中会输出：

```
/*  */

/**
 * 
 * @file:     
 * @author:   
 * @update:   
 * @note:     
 * @doc:      
*/
```

在 CSS 文件中输入`c1`，`c2`，会输出

```
/* ==========================================================================
   1级区块标题
   ========================================================================== */

/* --------------------------------------------------------------------------
   2级区块标题
   -------------------------------------------------------------------------- */
```

* 扩展代码片段

输入`@ff`，会输出：

```css
@font-face {
    font-family: 'FontName'; /* IE9 */
    src: url('FileName.eot');
    src: url('FileName.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
         url('FileName.woff') format('woff'), /* Chrome,Firefox */
         url('FileName.ttf') format('truetype'), /* Chrome,Firefox,Opera,Safari,Android, iOS 4.2+ */
         url('FileName.svg#FontName') format('svg'); /* iOS 4.1- */
}
```

输入`bgi+`，会输出：

```css
@media only screen and (-o-min-device-pixel-ratio: 2/1), /* Opera */
       only screen and (min--moz-device-pixel-ratio: 2), /* Firefox 16 之前 */
       only screen and (-webkit-min-device-pixel-ratio: 2), /* WebKit */
       only screen and (min-resolution: 192dpi), /* 不支持dppx的浏览器 */
       only screen and (min-resolution: 2dppx) /* 标准 */
{
    .selector{
        background-image:url();/* Retina */
        background-size: 图片宽度÷2px 图片高度÷2px;
    }
}
```

* 输出 cube 中的布局结构
输入`vbox`，会输出：

```html
<div class="vertical-box">
    <b class="vertical-hack"></b>
    <div class="vertical-content">
        <p>未知高度垂直居中模块</p>
    </div>
</div>
```

* 扩展和修复 emmet 错误的 CSS 声明

例如`font-smoothing`属性，输入`fsm`，会输出：

```css
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale; /* Firefox 25+ */
```

* 扩展 emmet 不支持的属性，比如`flex`，输入`dfx`，会输出：

```css
display: -webkit-box; /* Chrome 4+, Safari 3.1, iOS Safari 3.2+ */
display: -moz-box; /* Firefox 17- */
display: -webkit-flex; /* Chrome 21+, Safari 6.1+, iOS Safari 7+, Opera 15/16 */
display: -moz-flex; /* Firefox 18+ */
display: -ms-flex; /* IE 10 */
display: flex; /* Chrome 29+, Firefox 22+, IE 11+, Opera 12.1/17/18, Android 4.4+ */
```

所有输出代码都已经预定义光标路径，按`TAB`可以自动切换到下一个编辑点。

赶快试试吧(*^__^*) ！

