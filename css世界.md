## 为什么list-item元素会出现项目符号
* 在块级盒子加了一个附加盒子，而附加盒子（学名也叫标记盒子）专门存放项目符号。

## display:inline-table 的盒子
* 外面是“内联盒子”，里面是“table 盒子”。得到的就是一个可以和 文字在一行中显示的表格。 

##  width/height 作用在哪个盒子上 
* 内在盒子，也就 是“容器盒子”

## width:auto  四种不同的宽度表现
* 充分利用可用空间（\<div>、\<p>这些元素的宽度默认是 100%于父级容器）
* 收缩与包裹。(典型代表就是浮动、绝对定位、inline-block 元素或 table 元素)
* 收缩到最小(容易出现在 table-layout 为 auto 的表格中)
* 超出容器限制(内容很长的连续的英文和数字，或者内联 元素被设置了 white-space:nowrap)

## 流动性
* 内容很长的连续的英文和数字，或者内联 元素被设置了 white-space:nowrap
## 四个内在盒子
“内在盒子”又被分成了 4 个盒子，分别是 content box、padding box、border box 和 margin box
## 避免页面布局错位问题
* 书写方式约束，如使 用“宽度分离原则”。 （ CSS 中的 width 属性不与影响宽度的 padding/border（有 时候包括 margin）属性共存，`width 独立占用一层标签`，而 padding、border、margin 利用流动性在内部自适应呈现。）
```css
.box { width: 100px; border: 1px solid; } /*不采用这个方式*/


/*采用下面这种，width单独占一个标签，里面再占一个，让其宽度自适应*/
.father {    width: 180px; } 
.son {    margin: 0 20px;    padding: 20px;    border: 1px solid; } 

```
* 改变 width/height 作用细节的 box-sizing。，box-sizing 的作用就是可以把 width 作用的盒子变成其他几个， 
![](./imgs/1-1.png)
