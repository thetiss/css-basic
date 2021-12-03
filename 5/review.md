# 回顾

1 div是一个block 元素，宽度自动100% =》父级有多宽，它就有多宽；





# 课堂主题

## 5.1.2 

![image-20211202155929378](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202155929378.png)

## 5.2.1

![image-20211203142154448](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203142154448.png)

# task 1 半圆



# padding 知识点



# 文本text-*

## text-shadow: 文字阴影

```
    .title{
      height: 150px;
      width: 600px;
      background-color: #fff;
      border: 2px solid blue;
      font: 60px/120px '';
      text-align: center;
      /* X偏移 Y偏移 模糊半径 */
      text-shadow: 3px 3px 5px #f00;
    }    
```

![image-20211203135025300](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203135025300.png)

## over-flow: 文字超出

### /* overflow: visible; */ 默认值 超出部分要显示且滚动条在浏览器底部

```
    .text{
      height: 32px;
      width: 600px;
      background-color: #899;
      border: 2px solid blue;
      font: 16px/32px '';
      text-indent: 2em;
      text-decoration: underline;
      /* word 强制不换行 */
      white-space: nowrap;
      /* overflow: visible; */
    }
```

![image-20211203135343459](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203135343459.png)

###  overflow: hidden;  超出部分不显示

![image-20211203135456040](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203135456040.png)

### overflow: scroll; 滚动条在容器底部

![image-20211203135622509](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203135622509.png)

## white-space：空白区域如何定义 词与词间(e.g. 文字 文与字间有一个空白)  文字换行

多行文字默认自动换行

   /* white-space: nowrap; */

![image-20211203134334788](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203134334788.png)

```
      /* word 强制不换行 */
      white-space: nowrap;
```

![image-20211203134357723](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211203134357723.png)

## word-spacing: 词间距

## letter-spacing: 字母间距

## text-decoration: underline;

## text-indent: 2em; 首先缩进2字符；

首行缩进`text-indent: 2em;` 1em = 1个当前font-size;

## text-align 左右对齐 + line-height: 容器所在height => 左右上下居中

# 字体font(font-size/line-height）

要让文字在窗口中上下居中： line-height = 所在容器的高度；(因为行高会让文字上下居中，但不绝对)

![09232156-386cc51560954f7c8100ac89d272ae6f](file:///C:/Users/chenh/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

如上图，在font复合写法里：font-size和font-family是必写的



# background 知识点

## 5 复合样式

   `/* background-position / background-size e.g. 50px 100px / contain */`

   `background: #f00 url("imgs/film.jpg") no-repeat 50px 100px / contain;`

## 4 `background-attachment: fixed;`背景跟随

background-attachment: scroll ; // 默认要跟着盒子滚动

```
    body{
      width: 500px;
      height: 3700px;
      border:2px solid #899;
      background-image: url('imgs/film.jpg');
      background-repeat: no-repeat;
      // fixed属性 会让背景固定在可视窗口right 100px bottom 50px位置。
      background-position: right 100px bottom 50px;
      background-attachment: fixed;    }
```



滚动条最下面

![image-20211202181840282](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202181840282.png)

滚动条最上面

![image-20211202181814585](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202181814585.png)

## 3 `background-size: 100%;`背景尺寸

![image-20211202164250608](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202164250608.png)

### contain： 等比例缩放到合适尺寸，考虑图片展示效果。不一定覆盖整个div.

<img src="C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202180553541.png" alt="image-20211202180553541" style="zoom:67%;" />

### cover: 等比例缩放到合适尺寸，一定覆盖整个div.

<img src="C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202180516956.png" alt="image-20211202180516956" style="zoom:67%;" />

### 50%, 另外一个等比例缩放。

`图片宽度 = box.width * 50%` **高度是在宽度为50%后，等比例缩放效果，没有强制让其也是50%**

![image-20211202180023755](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202180023755.png)

### 100%, 另外一个等比例缩放。

![image-20211202180326629](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202180326629.png)

## 2 `background-position: 10px -150px;`背景位置

### 关键字定义位置：(center)(right|left  X )(bottom|top Y)

e.g. background-position: center; // 左右上下居中

e.g. background-position: right; === background-position: right [center] ;  // 靠右，上下居中



![image-20211202163417787](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202163417787.png)

<img src="C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202163850371.png" alt="image-20211202163850371" style="zoom:67%;" />

### 若位移尺寸，超过盒子的宽高，则背景图片会被截取

![image-20211202163308096](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202163308096.png)

### 图片左上角(0, 0)

### 参考坐标

![image-20211202163010700](C:\Users\chenh\AppData\Roaming\Typora\typora-user-images\image-20211202163010700.png)

## 1 `background-repeat: no-repeat;` 背景平铺

## 