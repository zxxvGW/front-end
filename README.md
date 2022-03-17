|           Ⅰ            |          Ⅱ           |  Ⅲ  |  Ⅳ  |           Ⅴ            |  Ⅵ   |
| :--------------------: | :------------------: | :-: | :-: | :--------------------: | :--: |
| [HTML](README.md#HTML) | [CSS](README.md#CSS) | JS  | ES6 | [VUE](./vue/README.md) | 网络 |

# HTML

#### 什么是 HTML

- 超文本标记语言 (英语：**H**yper**t**ext **M**arkup **L**anguage，简称：HTML ) 是一种用来结构化 Web 网页及其内容的标记语言。
- HTML 由一系列的元素（[elements](https://developer.mozilla.org/zh-CN/docs/Glossary/Element)）组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。

#### 语义化

- 对语义化的理解
  - 正确的标签做正确的事
  - web 语义化是指通过 HTML 标记表示页面所包含的新的，其中包括 HTML 标签的语义化和 CSS 命名的语义化。
  - HTML 语义化
    - 使用包含语义的标签如(h1-h6)恰当的表示文档结构
  - CSS 命名语义化
    - 为 html 标签添加有意义的 class，id 来补充未表达的语义
- 语义化的好处
  - 去掉样式后，页面也能呈现清晰的结构
  - 盲人使用读屏器更好地阅读
  - 方便 SEO
  - 方便项目团队的开发与维护

#### 标签类型

- 块级元素
  - 块级元素占据其父元素（容器）的整个宽度，因此创建了一个“块”。
  - 常见的块级元素：div,ol,ul,li,h1-h6,p
- 行内元素
  - 一个行内元素只占据它对应标签的边框所包含的空间。
  - 常见的行内元素有 a b span img strong sub sup button input label select textarea
- 空元素
  - 标签内没有内容的 HTML 标签被称为空元素。空元素是在开始标签中关闭的。
  - 常见的空元素有：br hr img input link meta

#### link 标签

- `link` 标签定义文档和外部资源的关系
- link 元素是空元素，它仅包含属性。
- 该元素只能存在于 head 部分
- 常见的作用就是加载一个 css 样式表

#### img 标签

- img 标签支持的格式
  - png | jpg | gif | Svg | Webp(谷歌发明的一种图片压缩格式)
- img 标签中的 alt 和 title 的区别
  - title 是当鼠标悬停到图片上显示的文字
  - alt 是< img>所特有的属性，主要用于当图片加载失败时显示的文字，搜索引擎会重点分析。
  - alt 是必需属性（但属性值可为空），title 非必需
- `src` 属性是**必须的**，它包含了你想嵌入的图片的文件路径。

#### label 标签

- label 标签主要是方便鼠标点击使用，扩大可点击的范围，增强用户操作体验

#### b 与 strong 的区别和 i 与 em 的区别？

- 从页面显示的效果来看，< b> 和< strong>都会将文字加粗 < i>和< em>都会将文字以斜体的方式展示文字
- < b>,< i> 是自然样式的标签 < strong>< em>是语义化的标签

#### iframe 有那些缺点？

- iframe 元素会创建包含另外一个文档的内联框架（即行内框架）。
- 优点：
  - 解决加载缓慢的第三方内容如图标和广告等的加载问题
  - Security sandbox
  - 并行加载脚本
- 缺点：
  - iframe 会阻塞主页面的 Onload 事件
  - 即时内容为空，加载也需要时间
  - 没有语意

#### meta 标签

- < meta> 元素可提供有关页面的元信息（meta-information），比如针对搜索引擎和更新频度的描述和关键词。

- ```html
  <meta charset="utf-8" /> 声明文档使用的字符编码
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" /> 优先使用 IE
  最新版本和 Chrome
  <meta name="description" content="不超过150个字符" /> 页面描述
  <meta name="keywords" content="" /> 页面关键词者
  <meta
    name="viewport"
    content="initial-scale=1, maximum-scale=3, minimum-scale=1, user-scalable=no"
  />
  为移动设备添加 viewport
  ```

#### link 和@import 的区别

- 从属关系的区别
  - @import 是 css 提供的语法规则，只有导入样式的作用。
  - link 是 html 提供的标签，不仅仅可以加载 css 文件，还能定义其他属性，引入网站图标。
- 加载顺序的区别
  - 加载页面时，link 标签引入的 css 会同步加载
  - @import 会在页面加载完毕后被加载
- 兼容性的区别
  - @import 是 css2.1 才有的语法，只有 ie5+才能识别，link 不存在兼容性问题
- dom 可控性区别
  - 通过 js 操作 dom 插入 link 标签来改变样式。@import 不能这样操作

#### href 和 src 的区别

- href：超文本引用
  - 标签：link a
- src：资源
  - 标签：img ，style，script，input，iframe
- href 相当与`建立一个通道`，让当前元素和引用资源进行联系。
- src 会把资源`下载`下来，替换当前元素嵌入到文档当中。

#### HTML5 新增的特性

- 绘画 canvas;
- 用于媒介回放的 video 和 audio 元素;
- 本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失;
- sessionStorage 的数据在浏览器关闭后自动删除;
- 语意化更好的内容元素，比如 article、footer、header、nav、section;
- 表单控件，calendar、date、time、email、url、search;
- 新的技术 webworker, websocket;
- 新的文档属性 document.visibilityState

#### 浏览器渲染流程

1. 解析 HTML 并构建 DOM 树
2. 构建 render 树
3. 布局 render 树
4. 绘制 render 树

#### margin-top 和 padding-top 的值是百分比时是如何计算的

- `margin-top`：相对最近的父元素块级的 width
- `padding-top`：相对于最近父级块级元素的 width

#### CSS 和 JS 如何阻塞 DOM 解析和渲染

- ` css` 不会阻塞 DOM 的解析，但是会阻塞 DOM 的渲染。
- `js` 阻塞 DOM 解析，但浏览器会”偷看“DOM，预先下载相关资源
- 浏览器遇到＜ script ＞标签且没有 defer 或者 async 属性的标签时，会触发页面渲染，因而如果前面的 css 资源尚未加载完毕时，浏览器会等待它加载完毕再执行脚本

# **CSS**

#### 什么是 CSS

- CSS(层叠样式表) 是用来指定文档如何展示给用户的一门语言——如网页的样式、布局、等等。
- CSS 可以用于给文档添加样式 —— 比如改变标题和链接的[颜色](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color_value)及[大小](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-size)。它也可用于创建布局 —— 比如将一个单列文本变成包含主要内容区域和存放相关信息的侧边栏区域的[布局](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Layout_cookbook/Column_layouts)。它甚至还可以用来做一些特效，比如[动画](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Animations)。

#### **说一下盒模型**

- 盒子模型（IE 和 W3C 标准）都是由四部分组成，内容(content)，填充(padding),边距(margin),边框(border)四个部分组成
- 标准的盒子模型 ： 属性 width,height 只包括内容，不包括 border 和 padding
- IE 的盒子模型： 属性 width,height 包括 content，padding，border。
- 我们也可以使用 css3 新增的 box-sizing 属性来更改元素盒模型

#### **css 选择器**

- 选择器类型

  - ```html
    （1）id选择器（#myid） （2）类选择器（.myclassname）
    （3）标签选择器（div,h1,p） （4）后代选择器（h1 p）
    （5）相邻后代选择器（子）选择器（ul>li） （6）兄弟选择器（li~a）
    （7）相邻兄弟选择器（li+a） （8）属性选择器（a[rel="external"]）
    （9）伪类选择器（a:hover,li:nth-child）
    （10）伪元素选择器（::before、::after） （11）通配符选择器（*）
    ```

- 通配符选择器

  - ```
     * {
     margin : 0;
     }
    ```

- 标签选择器

  - ```css
    a {
      color : red;
    }

    <a>hello world </a>
    ```

- 类选择器

  - ```css
    .abc {
        width: 100px;
    }

    <div class="abc"></div>
    ```

- id 选择器

  - ```css
    #abc {
        width: 100px;
    }

    <div id="abc"></div>
    ```

- 后代选择器

  - ```css
    .aaa span{
        color: red;
    }

    <div class="aaa">
    	<span> abc</span>
    </div>
    ```

- 子元素选择器

  - 子元素选择器只能选择作为某元素的最近一级子元素。

  - ```css
     .abc > a {
      color: red;
     }

    <div class="abc">
        <a href="#"></a>
        <p>
          <a href="#"></a>
        </p>
    </div>

    ```

- 并集选择器

  - ```css
    div,span {
        color: red;
    }

    <div class="abc"></div>
    <span>aaa</span>
    ```

- 伪类选择器

  - ```css
    <a href="#"></a>

    a:link {}  选择所有未被访问的链接

    a:visited {} 选择所有已经被访问的链接

    a:hover {} 选择鼠标指针位于其上的链接

    a:active {} 选择鼠标按下未弹起的链接
    ```

  - **注意事项**：为确保生效应该按照`LVHA`的顺序进行声明编写

- 伪元素选择器

  - ```css
    .a::after {
    	content: " ";
    	width: 10px;
    	height: 10px;
    }
    <div class="a"></div>
    ```

  - **伪类必须包含 content 属性**

#### 伪类和伪元素

- 在 css3 中使用单冒号来表示伪类，用双冒号来表示伪元素。但是为了兼容已有的伪元素的写法，在一些浏览器中也可以使用单冒号来表示伪元素
- 伪类一般匹配的是元素的一些**特殊状态**如：hover, link 等
- 伪元素一般匹配是元素的**特殊位置**比如 after before 等
  - 伪元素在页面效果是可见的，但是创建时并不会在文档树里面

#### 关于伪类 LHVA

- a 标签有四种 状态访问前，访问后，鼠标滑过，激活。分别对应 :link :visited :hover :active
- 链接未访问：
  - 鼠标滑过链接时，满足了 link，hover 状态，要改变颜色，就必须将: hover 放在: link 后面声明
  - 鼠标点击激活 a 链接，满足了 link，hover,active 三种状态，要显示 active 的样式只能将 active 声明放在 link,hover 后面。
- 链接访问过： 情况基本同上，只不过需要将:link 换成:visited
- 顺序可不可以变化：
  - 可以，但也只有:link 和:visited 可以交换位置，因为一个链接要么访问过要么没访问过，不可能同时满足，也就不存在覆盖的问题。

#### css 属性继承

- 每一个属性在定义中都给出了这个属性是否具有继承性，一个具有继承性的属性在没用指定的时候，会使用父元素的同属性的值来作为自己的值
- 具有继承属性：
  - 字体相关 font-size font-weight 等
  - 文本相关 color 和 text-align 等
  - 列表属性 list-style 等
  - 光标属性 cursor
  - 元素可见 visibility
- 当一个属性不是继承属性时，我们也可以通过设置属性值为 inherit 使它从父元素获取同名属性值

#### **css 权重与优先级**

- 当同一个元素上有多个指定的选择器，就会产生优先级

- 权重是由 4 组数据构成的

  - |        选择器         | 选择器权重 |
    | :-------------------: | :--------: |
    | 继承 或者 通配符 (\*) | 0，0，0，0 |
    |      元素选择器       | 0，0，0，1 |
    |  类选择器 伪类选择器  | 0，0，1，0 |
    |       ID 选择器       | 0，1，0，0 |
    |       行内样式        | 1，0，0，0 |
    |      ！important      |   无穷大   |

  - **继承的权重为 0** 如果该元素没有被直接选中，不管父亲权重有多高，子类得到的权重都是 0

#### **css 水平、垂直居中的写法，请至少写出 4 种？**

- _水平居中_
  - 行内元素: `text-align: center`
  - 块级元素: `margin: 0 auto`
  - `position:absolute` +left:50%+ `transform:translateX(-50%)`
  - `display:flex + justify-content: center`
- _垂直居中_
  - 设置 line-height 等于 height
  - `position：absolute` +top:50%+ `transform:translateY(-50%)`
  - `display:flex + align-items: center`
  - display:table+display:table-cell + vertical-align: middle;

#### **1rem、1em、1vh、1px 各自代表的含义？**

- > rem

  - rem 是全部的长度都相对于根元素<html>元素。通常做法是给 html 元素设置一个字体大小，然后其他元素的长度单位就为 rem。

- > em

  - 子元素字体大小的 em 是相对于父元素字体大小
  - 元素的 width/height/padding/margin 用 em 的话是相对于该元素的 font-size

- > vw/vh

  全称是 Viewport Width 和 Viewport Height，视窗的宽度和高度，相当于 屏幕宽度和高度的 1%，不过，处理宽度的时候%单位更合适，处理高度的 话 vh 单位更好。

- > px

  px 像素（Pixel）。相对长度单位。像素 px 是相对于显示器屏幕分辨率而言的。

-

#### **画一个三角形？**

- 原理：

  - 由于 css 的边框是由四个三角组成的，我们画一个三角形可以让边框的三个位置的颜色变得透明

  - 实现

    ```css
    .a{
        width: 0;
        height: 0;
        border-width: 100px;
        border-style: solid;
        border-color: transparent #0099CC transparent transparent;
        transform: rotate(90deg); /*顺时针旋转90°*/
     }
    <div class="a"></div>
    ```

  - 效果

    ![css画三角形](./img/image-20211120151441681.png)

    ![css画一个三角](./img/image-20211120151529984.png)

#### **清除浮动**的几种方式，及原理？

- > 为什么要清除浮动

  - 由于父盒子很多情况下，不方便给高度，但是子盒子浮动由不占有位置，最后父盒子的高度变成了 0，就会影响标准流的盒子

- > 清除浮动方法

  1. 额外标签法：
     - 给浮动元素的末尾添加一个空的标签
     - 注意 这个元素必须是块级的标签
  2. 父级添加`overflow`：
     - 创建父级 `BFC`(overflow:hidden)
  3. `::after`伪元素法
  4. 父级设置高度

- > *BFC （*块级格式化上下文*）*，是一个独立的渲染区域，让处于 `BFC` 内部的元素与外部的元素相互隔离，使内外元素的定位不会相互影响。

  _触发条件:_

  - 根元素

  - `position: absolute/fixed`

  - `display: inline-block / table`

  - `float` 元素

  - `ovevflow !== visible`

- _规则:_

  - 属于同一个 `BFC` 的两个相邻 `Box` 垂直排列

- 属于同一个 `BFC` 的两个相邻 `Box` 的 `margin` 会发生重叠
  - `BFC` 的区域不会与 `float` 的元素区域重叠
  - 计算 `BFC` 的高度时，浮动子元素也参与计算
  - 文字层不会被浮动层覆盖，环绕于周围

#### display:none 和 visibility:hidden 的区别

- display:none，
  - 渲染树不会包括该渲染对象，因此不会在页面中占据位置，也不会绑定监听事件
  - 是非继承属性，子孙节点消失是由于元素从渲染树消失，更改子孙节点的属性也无法显示。
  - 修改 display 属性通常会造成文档的重排(reflow)和重绘(repaint)
- visibility：hidden，
  - 元素在页面仍然会占据空间，但是不会响应绑定事件
  - 继承属性，子节点默认继承了父节点的属性，更改成 visibility：visible 可以让节点显示
  - 修改 visibility 属性只会造成文档的重绘(repaint)

#### position 定位属性

- **`position`**属性用于指定一个元素在文档中的定位方式。[`top`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/top)，[`right`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/right)，[`bottom`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/bottom) 和 [`left`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/left) 属性则决定了该元素的最终位置。

#### position:relative 和 position:absolute 的区别

- `position:relative`不改变页面布局的前提下调整元素位置（因此会在此元素未添加定位时所在位置留下空白）
- `position:absolute` 元素会被移出正常文档流，并不为元素预留空间，通过指定元素相对于最近的非 static 定位祖先元素的偏移，来确定元素位置。

#### position:static 的作用

- 该关键字指定元素使用正常的布局行为，即元素在文档常规流中当前的布局位置。
- 清除其他定位的属性

#### **css3 新的特性？**

- RGBA 和透明度

  - 是 RGB 颜色模型的一个扩展。本质上，在设置元素中添加了一个 alpha 通道，即一个表示除红色、绿色和蓝色三种颜色之外的透明度的通道。

- background 属性

  - background-image：设置元素的背景图像。
  - background-origin：规定背景图片的定位区域。
  - background-size ：规定背景图片的尺寸。
  - background-repeat：设置是否及如何重复背景图像。

- word-wrap 属性

  - word-wrap 属性允许长单词或 URL 地址换行到下一行。

- text-shadow 属性

  - 向文本设置阴影。

- **border-radius 属性**

  - 该属性允许您为元素添加圆角边框！

  - 基础用法

    ```css
    border-radius: 50%;
    ```

- **box-shadow 属性**

  - box-shadow 属性：向框添加一个或多个阴影。（盒阴影）

#### **calc**, support, **media**各自的含义及用法？

- @support 主要是用于检测浏览器是否支持 CSS 的某个属性，其实就是条件判断，如果支持某个属性，你可以写一套样式，如果不支持某个属性，你也可以提供另外一套样式作为替补。
- calc() 函数用于动态计算长度值。 calc()函数支持 "+", "-", "\*", "/" 运算；
- @media 查询，你可以针对不同的媒体类型定义不同的样式。

#### 过渡动画和帧动画

|            | 触发条件 |       状态       | css 属性 | 遍历循环(持续) | js 结合 | 子属性 |
| :--------: | :------: | :--------------: | :------: | :------------: | :-----: | :----: |
| transition |   需要   | 两种(开始，完成) | 不可修改 |      无法      |  易于   |   少   |
| animation  |   无需   |      无限制      |  可修改  |      允许      | 不易于  |   多   |

#### 外边距塌陷

- 外边距塌陷：当两个块级元素设置 margin-top 和 margin-bottom 时会只有最大的生效
  - 外边距塌陷只存在与垂直方向上
  - 只有`块级元素`才会出现，行内，行内块都不会
- 计算规则：
  1. 正数 && 正数 ：最大值
  2. 负数 && 负数 ：绝对值的最大值
  3. 正数 && 负数 ：相加的和
- 解决：
  - `position` + ` margin` : 对父元素添加 position：relative，子元素设置 position：absolute
  - 设置元素 display：inline-block
  - overflow：hidden
  - 边框 border
  - 空元素

#### **BFC(块级格式化上下文：block formatting context)**

- BFC 是一个独立的布局环境，可以理解为一个容器，在这个容器中按照一定规则进行物品摆放，并且不会影响其它环境中的物品。
- 如果一个元素符合触发 BFC 的条件，则 BFC 中的元素布局不受外部影响。
- 创建 BFC
  1. 根元素或包含根元素的元素
  2. 浮动元素 float ＝ left|right 或 inherit（≠none）
  3. 绝对定位元素 position ＝ absolute 或 fixed
  4. display ＝ inline-block|flex|inline-flex|table-cell 或 table-caption
  5. overflow ＝ hidden|auto 或 scroll(≠visible)

#### **flex 布局**

- flex 布局是 CSS3 新增的一种布局方式，我们可以通过将一个元素的 display 属性值设置为 flex 从而使它成为一个 flex
  容器，它的所有子元素都会成为它的项目。
- 一个容器默认有两条轴，一个是水平的主轴，一个是与主轴垂直的交叉轴。我们可以使用 flex-direction 来指定主轴的方向。
  我们可以使用 justify-content 来指定元素在主轴上的排列方式，使用 align-items 来指定元素在交叉轴上的排列方式。还
  可以使用 flex-wrap 来规定当一行排列不下时的换行方式。
- 对于容器中的项目，我们可以使用 order 属性来指定项目的排列顺序，还可以使用 flex-grow 来指定当排列空间有剩余的时候，
  项目的放大比例。还可以使用 flex-shrink 来指定当排列空间不足时，项目的缩小比例。

# **JS 基础**

#### JS 的数据类型

- js 中一共有七种基本数据类型：（考虑 ES6）
  - Undefined、Null、Boolean、Number、String
  - ES6 新增了 Symbol，BigInt
- 一种复杂数据类型：Object
  - 如 Array、Date 等数据类型都可以理解为 Object 类型的子类

#### || 和 &&

- 逻辑操作符
- || 如果条件判断结果为 `true` 返回一个**操作数的值** ，如果为`false` 就返回第二个**操作数的值**
- && 如果条件判断结果为`true` 返回第二个**操作数的值**，如果为`false` 就返回第一个**操作数的值**
- || 和 && 返回的是其中一个操作数的值，而不是条件判断的结果。

#### null 和 undefined 的区别

- null 和 undefined 都是基本数据类型
- undefined 代表是未定义，一般变量声明了但还没有定义的时候会返回 undefined
- null 表示空对象，主要用于赋值给一些可能会返回对象的变量，作为初始化。
- typeof null 会返回 “Object”
- `null == undefined => true`
- `null === undefined => false`

#### 什么是 BOM，DOM

- DOM 是值文档对象模型，它是指把文档当作一个对象来对待。DOM 是载入到浏览器中的文档模型，以节点树的形式来表现文档，每个节点代表文档的构成部分
  - **常用的对象或方法**： document.append(增加一个元素)，document.querySelector(查找一个元素)，document.addEventListener(事件监听)
- BOM 是指浏览器对象模型，它是指将浏览器当作一个对象来对待，这个对象主要定义了与浏览器进行交互的法和接口。
  - BOM 的核心是 window，而 window 对象具有双重角色，它既是通过 js 访问浏览器窗口的一个接口，又是一个 Global（全局）对象。
  - **常用的对象或方法**： location 对象、navigator 对象、screen 对象 window.alert(),`window.setTimeout()` **setTimeOut 是是浏览器实现的方法**

#### JavaScript 标准事件模型

- 事件捕获 ===> 事件处理 = ==> 事件冒泡

#### `+`操作符

- 如果 + 的其中一个操作数是字符串（或者通过以上步骤最终得到字符串），则执行字符串拼接，否则执行数字
  加法。
- 那么对于除了加法的运算符来说，只要其中一方是数字，那么另一方就会被转为数字。

#### [1,2]+[3,4] ?

- ```javascript
  console.log([1, 2] + [3, 4]);
  // 1,23,4
  ```

- 其中一个操作数是对象(包括数组)，首先会调用 ToPrimitive 抽象操作，该方法会再调用[[DefaultValue]],以数字作为上下文

- 数组的 valueOf()操作无法得到简单基本类型值，于是转而调用 toString(),两个数组变成了 “1，2 ”和 “3，4”，+拼接后变成了 “1,23,4 ”

#### == 操作符的强制类型转换规则

- 1. 字符串和数字之间相比较时，将字符串转换成数字之后比较
  2. 其他类型与 Boolean 值比较时，先将 Boolean 值转换成数字，再比较
  3. null 和 undefined 相比较时，结果为**true**，其他值和他们比较时都为**false**
  4. 一个操作值为 NaN，则全部返回**false**，NaN== NaN ==> **false**
  5. 当比较两个对象时，比较的是他们的引用是不是指向的是同一个对象

#### 隐式强制类型转换为布尔值

- 发生情况
  1. if (...) 语句中的条件判断表达式
  2. for( ... ; ... ; ...; )语句中的条件判断表达式(第二个)
  3. while ( ... ) 和 do ( ... ) 循环中的条件判断表达式
  4. ？... ：... 中的条件判断表达式
  5. 逻辑运算符 || 和 && 左边的操作数

#### 说一下闭包？

- 闭包的实质是因为函数嵌套而形成的作用域链
- 闭包的定义即：函数 `A` 内部有一个函数 `B`，函数 `B` 可以访问到函数 `A` 中的变量，那么函数 `B` 就是闭包

#### 数据类型转换

- | 数据类型  | 转换为 true 的值 | 转换为 false 的值 |
  | --------- | ---------------- | ----------------- |
  | Boolean   | true             | false             |
  | String    | 非空字符串       | 空字符串          |
  | Number    | 任何非零数字值   | 0 和 NaN          |
  | Object    | 任何对象         | null              |
  | undefined |                  | undefined         |

#### instanceof 的作用，与 typeof

- instanceof 运算符用于判断构造函数的 prototype 属性是否出现在对象的**原型链中**的任何位置
- typeof 判断所有变量的类型，返回值有 number，boolean，string，function，object，undefined。
- typeof 对于丰富的对象实例，只能返回"Object"字符串。

#### 变量提升和函数提升

- 函数声明，变量声明都会被提升到作用域的顶处。
- 当出现名称相同时，优先级为：**变量提升** < **函数声明** < **变量赋值**
- 函数表达式不会被提升

#### 原型和原型链

- 对象的\_ _ proto_ \_ 属性

  - js 中的每一个对象都有一个特殊的内置属性[[prototype]]
  - 我们可以通过 obj.\_ _proto_ \_或者 Object.getPrototypeOf 获取到

- 函数的原型`prototype`

  - 所有的函数都有一个 prototype 属性

  - ```javascript
    var student = new Person();

    console.log(student.__proto__ === Person.prototype); // true
    ```

- 构造函数`constructor`

  - 在 js 中我们使用一个构造函数来创建一个新对象。
  - 每一个构造函数内都有一个 prototype 属性值，这个属性值是一个对象，这个对象包含了可以由该构造函数的所有实例共享的属性和方法。

- 原型链

  - 当我们访问一个对象的属性时，如果这个对象内部不存在这个属性，那么它就会去它的原型对象里找这个属性，这个原型对象又
    会有自己的原型，于是就这样一直找下去，也就是原型链的概念。

#### JS 继承的方式(todo)

#### 函数调用的方式(todo)

#### this 指向(todo)

#### 如何改变 this 的指向

- bind
- call
- apply

#### 回调地狱除了在网络请求中还可能出现在什么地方(todo)

#### JS 内置对象(todo)

#### 回流(reflow)和重绘(repaint)

- reflow : 例如某个子元素的样式发生变化，直接影响到其父元素以及往上追溯很多的祖先元素(包括兄弟元素)，这个时候浏览器要重新渲染这个子元素相关联的所有元素的过程称为回流。
- repaint： 如果只改变某个元素的背景色，文字颜色，边框颜色等不影响他周围或内部的属性，将会引起浏览器的 repaint
- **reflow 几乎是无法避免的**。
- 下面情况将会导致 reflow 发生
  1. 改变窗口的大小
  2. 改变文字的大小
  3. 内容的改变，如用户在输入框中输入
  4. 激活伪类，如：hover
  5. 操作 class 属性
  6. 脚本 dom 操作
  7. 计算 offsetWidth，和 offsetHight
  8. 设置 style 属性

#### 数组方法

- **`push` 尾部添加**，返回**新的长度**
- **`pop` 尾部删除**，返回**被删除的元素**
- **`shift` 首部删除**，返回**被删除的元素**
- **`unshift` 首部添加**，返回**新的长度**

#### NaN 相关

- NaN == NaN //` false`
- NaN === NaN // false
- `indexOf`方法无法识别数组的 NAN 成员
  - indexOf 使用严格相等的运算符 (===)
  - [NaN].indexOf(NaN) // `-1`
- Set 中加入值时认为 NAN 等于自身
- Object.is()认为 NaN 等于 NaN
- ES7 新增数组的实例方法，includes()方法认为 NaN 等于自身
  - [1,2,Nan].includes(NaN) // `true`

#### eval 函数

- eval 将返回对最后一个表达式的求值结果

####  arguments

- arguments 是函数的内置对象，是一个类数组

- 有 length，可以被遍历

- 无 pop() push()等方法，arguments 是类数组，不是一个真正的数组

- 您还可以使用[`Array.from()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/from)方法或[扩展运算符](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)将参数转换为真实数组：

- ```javascript
  var args = Array.from(arguments);
  var args = [...arguments];
  ```



# DOM

#### Event(todo)

#### currentTarget 和 target

- e.target指向的是**触发**的对象
- e.currentTarget指向的是**绑定**的对象

# ES6 基础

#### ES6 新增特性

- 新关键字 let const
- Promise
- 模板字符串
- class 关键字
- 箭头函数
- generator
- Map/Set
- 模块化
- 数组新方法

#### 暂时性死区

- 使用 let，cconst 声明的变量在声明前，变量是不可以进行访问的
- 访问则会出现 TDZ（temporal dead zone）暂时性死区

#### 箭头函数与普通函数的区别

- 箭头函数相对于普通函数书写比较简单
- 箭头函数是匿名的
- 箭头函数没有[[constructor]]方法，也即不能使用 new 关键字来创建对象
- 箭头函数是不绑定 arguments 对象
- this 的指向，箭头函数不绑定 this，当访问到 this 时会向上面的作用域去查找 this

#### promise(todo)

#### axios 的封装(todo)

# 网络

#### HTTP

- HTTP(**超文本传输协议**)

- 状态码

  | 状态码 |    含义    |                                    详情                                    |
  | :----: | :--------: | :------------------------------------------------------------------------: |
  |  200   |    成功    |                     服务器成功处理了请求，**返回内容**                     |
  |  204   |   无内容   |                 服务器成功处理了请求，但是**没有返回内容**                 |
  |  301   | 永久重定向 |          请求的网页已经移动到了新位置，服务器自动将请求转到新地址          |
  |  302   | 临时重定向 | 服务器目前从不同的位置的网页响应请求，但请求者应继续使用原有的位置进行请求 |
  |  304   |  资源缓存  |                                                                            |
  |  400   |  错误请求  |                  服务器不理解请求的语法（一般是参数错误）                  |
  |  401   |   未授权   |                                                                            |
  |  403   |    禁止    |                服务器拒绝请求（一般是客户端的用户权限不够）                |
  |  404   |   未找到   |                              服务器找不到资源                              |
  |  500   | 服务器错误 |                              服务器内发生错误                              |

- 响应首部

  - content-type

#### HTTPS(todo)

#### TCP 三次握手四次挥手

- 因为 TCP 连接时全双工的，即通信的双方都可以向对方发送信息和接收信息，所以断开连接需要双方确认
- SYN：`synchronization`（同步）ACK : `acknowledgment`（确认）FIN：（完成）
- **三次握手**

  - 第一次握手：`客户端`向服务端发送一个 SYN 连接请求的报文，SYN 的标志位为１，生成随机序号，作为客户端数据的初始序号

  - 第二次握手：`服务端`收到客户端发送的 SYN 报文，服务器首先会为该连接分配 TCP 缓存和变量，让后向客户端发送 SYN+ACK 信号，服务器生成自己的序号，并将第一次握手时客户端生成的`序号+1`做为确认号，一起发送给客户端。

  - 第三次握手：`客户端`接收到服务端的 SYN+ACK 信号，开启客户端的 ACK 信号。将序号+1 ,确认号:是服务器发送的序号+1

  - |            |        流向        |  报文段  |          序号和确认号           |
    | :--------: | :----------------: | :------: | :-----------------------------: |
    | 第一次握手 | 客户端 ===> 服务器 |   SYN    |       序号：N(客户端初始)       |
    | 第二次握手 | 服务器 ===> 客户端 | SYN+ ACK | 序号：M(服务端初始) 确认号：N+1 |
    | 第三次握手 | 客户端 ===> 服务端 |   ACK    |      序号：N+1 确认号：M+1      |

- **四次挥手**

  - 第一次挥手：`客户端` 发送 FIN+ ACK 报文段，
  - 第二次挥手：` 服务端` 发送 ACK 来进行确认，序号用对方的确认号，确认号用对方的序号+1
  - 第三次挥手：`服务端`可能还有未发送的数据，等到服务端发送完数据，服务端发送一个 FIN+ACK l 来进行最后的确认，此时的序号和确认号不变。
  - 第四次挥手：`客户端` 得到最终的结果后发送 ACK 来进行确认，序号用对方的确认号，确认号用对方的序号+1

  - |            |        流向        | 报文段  | 序号和确认号          |
    | :--------: | :----------------: | :-----: | :-------------------- |
    | 第一次挥手 | 客户端 ===> 服务器 | FIN+ACK | 序号：N 确认号：M     |
    | 第二次挥手 | 服务器 ===> 客户端 |   ACK   | 序号：M 确认号：N+1   |
    | 第三次挥手 | 服务器 ===> 客户端 | FIN+ACK | 序号：M 确认号：N+1   |
    | 第四次挥手 | 客户端 ===> 服务端 |   ACK   | 序号：N+1 确认号：M+1 |

  - TCP 使用四次挥手的原因是因为 TCP 的连接是全双工的，所以需要双方分别释放到对方的连接，单独一方的连接释放，只代 表不能再向对方发送数据，连接处于的是半释放的状态。

  - 最后一次挥手中，客户端会等待一段时间再关闭的原因，是为了防止发送给服务器的确认报文段丢失或者出错，从而导致服务器 端不能正常关闭。

#### no-cache 和 no-store

- `no-cache`：表示可以进行缓存，但是每次需要和服务器进行确认，同时代理服务器也不能对资源进行缓存
- `no-store`：表示浏览器不要缓存资源，每次向服务器请求资源

#### HTTP1.0 和 HTTP1.1 的区别

- 连接方面：HTTP1.1 默认使用持久连接，http1.0 默认使用非持久连接。
- 资源请求方面的区别，在 http1.0 中，存在一些浪费带宽的现象，例如客户端只是需要某个对象的一部分，而服务器却将整个对象送过来了。HTTP1.1 支持断点连接。
- 缓存方面的区别，在 http1.0 中主要使用 header 里的 If-Modified-Since,Expires 来做为缓存判断的标准，http1.1 则引入了更多的缓存控制策略例如 Etag、If-Unmodified-Since、If-Match、If-None-Match 等更多可供选择的缓存头来控制缓存策略。
- http1.1 中还新增了 host 字段，用来指定服务器的域名。
- http1.1 相对于 http1.0 还新增了很多方法，如 PUT、HEAD、OPTIONS 等。

#### GET 和 POST 的区别

- 从应用场景来说：
  - GET 请求一般用于对服务器资源不会产生影响的场景，比如请求一个网页
  - POST 请求一般用于对服务器资源会产生影响的情景。比如注册用户这一类的操作。
- 缓存
  - 一般浏览器会对 GET 请求缓存，很少对 POST 请求缓存
- 发送的报文格式
  - GET 请求的报文实体为空
  - POST 报文中实体部分一般为向服务器发送的数据。
- Get 请求也可以将请求的参数放入 url 中向服务器发送，这样的做法相对于 Post 请求来说，一个方面是不太安全，
  因为请求的 url 会被保留在历史记录中。
- url 还有长度限制
- 还有就是 post 的参数传递支持更多的数据类型。
