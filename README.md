# Emmet plus 让 Emmet 更强大

![Emmet plus animation demo](http://gtms01.alicdn.com/tps/i1/T1oIAwFXtgXXa1BMjv-707-735.gif)

## 如何使用？

以 Sublime Text 2 为例

1. 首先请确保已经安装了 Emmet， 并可以正常使用。
2. 打开菜单 ```Preferences```→```Package Settings```→```Emmet```→```Settings-User```
3. 复制```Emmet.sublime-settings```文件中的所有内容，粘贴到上面打开的```Settings-User```中
4. 保存后重启 Sublime Text
5. 打开一个 CSS 文件，输入```cm```，如果成功生成了如下注释，安装成功

   ```css
    /**
     * 
     * @file:     
     * @author:   
     * @update:   
     * @note:     
     * @doc:      
     */
   ```
6. 尽情享受吧！

> Sublime Text 3 如果无法使用，欢迎反馈

## 扩展了哪些功能？

* 统一的注释风格，以[css-creating](https://github.com/yisibl/css-creating)为参考。

    例如输入`c`，`cm`

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
    display: -ms-flexbox; /* IE 10 */
    display: flex; /* Chrome 29+, Firefox 22+, IE 11+, Opera 12.1/17/18, Android 4.4+ */
    ```

* 增加了更多的 CSS 单位:
    > c:ch, d:deg, g:grad, r:rad, t:turn

* 增加更多的 CSS 简写:
    > n:none, ih:inherit, ii:initial, db:double, u:unset

* 增加了更多的没有单位的 CSS 属性:
    > animation-iteration-count, counter-increment, font-size-adjust, flex-grow, flex-shrink, order, column-count, orphans, widows, shape-image-threshold, mask-box-outset


所有输出代码都已经预定义光标路径，按 ```TAB``` 键可以自动切换到下一个编辑点。

赶快试试吧(*^__^*) ！

