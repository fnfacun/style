# 样式（Style）

# 字体

## 字体简写方式
```css
font: [font-style] [font-variant] [font-weight] [font-size]/[line-height] [font-family];
```

## 定义字体大小（font-size）
- xx-small（最小）
- x-small（较小）
- small（小）
- medium（正常）
- large（大）
- x-large（较大）
- xx-large（最大）
- larger（增大）
- smaller（减少）
- length（尺寸）

## 定义字体颜色（color）
取值包括颜色名、十六进制值、RGB/RGBA 等颜色函数
- color: color

## 定义字体粗细（font-weight）
- normal（默认值，相当于取值 400）
- bold（粗体，相当于取值 700）
- bolder（较粗）
- lighter（较细）
- 100 - 900（越大越粗，相反越细）

## 定义艺术字体（font-style）
- normal（默认值）
- italic（斜体）
- oblique（倾斜）

## 定义修饰线（text-decoration）
- none（没有）
- normal（默认值，表示无装饰线）
- underline（下划线效果）
- blink（闪烁效果）
- overline（上划线效果）
- line-through（贯穿线效果）
### text-decoration-line
- 设置装饰线的位置（ none、underline、overline、line-through、blink）
### text-decoration-color
- 设置装饰线的颜色
### text-decoration-style
- 设置装饰线的形状（ solid、double、dotted、dashed、wavy(波浪线) ）
### text-decoration-skip
- 设置文本装饰线必须略过内容中的那些部分
### text-decoration-position
- 设置对象中的下划线的位置

## 定义字体的变体（font-variant）
仅支持拉丁字体，中文字体没有大小写效果区分
- normal（默认值）
- small-caps（小型的大写字母字体）

## 定义大小写字体（text-transfrom）
- none（默认值，表示无转换发生）
- capitalize（表示每个单词的第一个字母转换为大写）
- uppercase（表示把所有字母都转换为大写）
- lowercase（表示把所有字母都转换为小写）

## 定义文本对齐（text-align）
定义文本的水平对齐方式，该属性仅对行内对象有效，如文本、图像、超链接，如果想让块元素对齐显示，如设计网页居中显示，需要特殊方法。
- left、start（默认值，左对齐）
- right、end（右对齐）
- center（居中对齐）
- justify（两端对齐）

## 定义垂直对齐（vertical-align）
world 对准 hello ---- 的基线
```html
<p>hello<span>world</span></p>
```
- auto（将根据 layout-flow 属性的值对齐对象内容）
- baseline（表示默认值，表示将支持 valign 特性的对象内容与基线对齐）
- sub（表示垂直对齐文本的下标）
- super（表示垂直对齐文本的上标）
- top（表示将支持 valign 特性的对象的内容与对象顶部对齐）
- text-top（表示将支持 valign 特性的对象的文本与对象顶部对齐）
- middle（表示将支持 valign 特性的对象的内容与对象中部对齐）
- bottom（表示将支持 valign 特性的对象的内容与对象底部对齐）
- text-bottom（表示将支持 valign 特性的对象的文本与对象底部对齐）
- length（表示由浮点数和单位标识组成的长度值或者百分比）

## 定义文本间距（letter-spacing、word-spacing）
这两个属性的取值都是长度值，由浮点数字和单位标识符组成，默认值为 normal，表示默认间隔
### letter-spacing
- 定义字距
### word-spaing
- 定义词距，以空格为基准进行调节，如果多个单词被连在一起，则视为一个单词，如果汉字被空格分隔，则分隔的多个汉字被视为不同的单词


## 定义行高（line-height）
- normal（默认值，一般为 1.2em）
- length（表示百分比数字，或者浮点数和单位标识符组成的长度值，允许为负值）

## 定义首行缩进（text-index）
- length（表示百分比数字，或者浮点数和单位标识符组成的长度值，允许为负值。建议在设置缩进单位时，以 em 为位置单位，它表示一个字距，这样比较精确确定首行缩进效果）


## 定义图像大小
当为图像仅定义宽度和高度，则浏览器能够自动调整纵横比，使宽和高能够协调缩放，避免图像变形。
- width（宽度）
- height（高度）

## 定义图像边框（border）

```css
div { border: 1px solid red }
```

### border-width
- 定义边框粗细
- ```css
  border-width: 10px 20px 30px 40px;
  /* 上10px 右20px 下30px 左40px */
  ```
### border-style
- 定义边框样式（ solid（实线）、double（双线框）、groove（立体凹槽）、rideg（立体凸槽）、inset（立体凹边）、outset(立体凸边) ）
### border-color
- 定义图像颜色
### opacity
- 不透明度

## 定义圆角特效（border-radius）
- none（初始值）
- length（浮点数字和单位标识符组成的长度值，不可为负值）
### border-top-left-radius
- 定义左上角的圆角
### border-top-right-radius
- 定义右上角的圆角
### border-bottom-left-radius
- 定义左下角的圆角
### border-bottom-right-radius
- 定义右下角的圆角


## 定义阴影特效（box-shadow）
```css
box-shadow: inset 10px 10px 4px orange;
/* 内阴影 水平偏移 垂直偏移 阴影大小 阴影颜色 */
```
- none（初始值，表示没有阴影）
- inset（内阴影）
### 阴影叠加
```css
box-shadow: -10px 0 12px red,
            10px 0 12px blue,
            0 -10px 10px pink,
            0 10px 12px green
```
### 阴影兼容
```css
-moz-box-show: inset 10px 10px orange;			/* 兼容 Gecko 引擎 */
-webkit-box-show: inset 10px 10px 4px orange;	/* 兼容 Webkit 引擎 */
```

