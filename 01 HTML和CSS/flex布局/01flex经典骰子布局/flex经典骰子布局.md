### 考试题目

1. 补全 index.html 文件空缺的 css 代码。
2. 骰子 1：使用 `justify-content` 与 `align-items` 属性实现。
3. 骰子 2：使用 `justify-content`、`flex-direction` 与 `align-items` 属性实现。
4. 骰子 3：使用 `justify-content`、`align-self` 与 `align-items` 属性。
5. 骰子 4、5、6、7、9 布局结构类似：使用 `justify-content`、`align-self`、 `flex-direction` 与 `align-items` 属性实现。
6. 骰子 8：使用 `justify-content`、`flex-wrap`、`flex-basis` 与 `align-items` 属性实现。

根据试题需求中要求的属性进行页面布局，无需过多样式设置。按以上要求完成以下效果（页面整体宽度 `1024px`）：

![https://doc.shiyanlou.com/courses/uid1693782-20211020-1634693026688]()

关键尺寸批注如下：（可以通过在图片上右键-》“在新标签页打开图片”，或在右键-》复制图片地址后到浏览器新标签页打开并放大图片，查看关键尺寸）

![https://doc.shiyanlou.com/courses/uid1693782-20211018-1634538921755]()

### 考核点：flex 布局

### 考核点：css 选择器

#### 四种基本选择器

1. 标签选择器

2. ID 选择器

3. 类选择器

4. 通配符\*

#### css 的几种高级选择器

1. 后代选择器：空格隔开
2. 交集
3. 并集

一些 css3 选择器

1. 子选择器，用符合>表示

```css
div > p {
  color: red;
}
```

div 的儿子 p，和 div 的后代 p 的截然不同

能够选择：

```html
<div>
  <p>我是div的儿子</p>
</div>
```

不能选择：

```html
<div>
  <ul>
    <li>
      <p>我是div的重孙子</p>
    </li>
  </ul>
</div>
```

2. 序选择器

```html
<ul>
  <li class="first">项目</li>
  <li>项目</li>
  <li>项目</li>
  <li>项目</li>
  <li>项目</li>
  <li>项目</li>
  <li>项目</li>
  <li>项目</li>
  <li>项目</li>
  <li class="last">项目</li>
</ul>
```

设置无序列表`<ul>`中的第一个`<li>`为红色：

```css
<style type="text/css">
    ul li:first-child {
        color: red;
    }
</style>
```

设置无序列表`<ul>`中的最后一个`<li>`为红色：

```css
ul li:last-child {
  color: blue;
}
```

3. 下一个兄弟选择器，用+表示

```html
<h3>我是一个标题</h3>
<p>我是一个段落</p>
<p>我是一个段落</p>
<p>我是一个段落</p>
<h3>我是一个标题</h3>
<p>我是一个段落</p>
<p>我是一个段落</p>
<p>我是一个段落</p>
<h3>我是一个标题</h3>
<p>我是一个段落</p>
<p>我是一个段落</p>
<p>我是一个段落</p>
<h3>我是一个标题</h3>
```

```css
<style type="text/css">
    h3 + p {
        color: red;
    }
</style>
```

上方的选择器意思是：选择的是 h3 元素后面紧挨着的第一个兄弟。
