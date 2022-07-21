# HTML 入门笔记 1

## 关于 WWW

1. 起源

   * WWW 是李爵士（Tim Berners-Lee）在1990年左右基于互联网发明的万维网：World Wide Web 像世界那么宽的网
   * 旨在让每个人输入网址就能看到网页：WWW=URL（网址）+HTTP（其他）+HTML（网页）

2. 影响
   * 马云于1995年去美国，回国后创办中国黄页，于1999年创办阿里巴巴，于2003年创办淘宝，于2004年创办支付宝
   * 1995年至2000年之间，美国发生了.com泡沫
   * 1998年腾讯创立，2000年百度创立

## 关于 HTML
1. HTML：HyperText Markup Language 超文本标记语言

2. 新建文件夹，新建 index.html 文件，输入 html:5 快速生成 HTML 框架

   ![HTML 框架](html%20框架.png)

## 英语小课堂

![html 英语小课堂](html%20英语小课堂.png)

## 常用章节标签

1. article 文章
2. header 头部
3. div 划分
4. main 主要内容
5. h1~h6 标题
6. section 章节
7. p 段落
8. aside 旁支内容
9. footer 脚部

![常用章节标签](常用章节标签效果展示.png)

## 全局属性

1. class 给元素分类，标记一下

   ![class 作用](class%20作用.png)

2. contenteditable 使得任意元素可被编辑

   ![contenteditable 作用1](contenteditable%20作用1.png)

   ![contenteditable 作用2](contenteditable%20作用2.png)

3. hidden 隐藏任意元素

   ![hidden 作用](hidden%20作用.png)

4. id 与 class 功能同

   * 针对全页面唯一元素时用id，不唯一时用class，但是当
   * 不唯一时用id不会被报错，会让人误以为全局只有唯一此元素，所以
   * 尽量不使用id（在CSS和JS中尽可能用class）

5. style 设置元素样式

   * style 样式优先级高于CSS操作
   * JS 操作优先级高于 style 样式

6. tabindex

   * 通过在元素后设置"tabindex=具体数字"，来控制tab的顺序
   * 应对场景：用户鼠标失灵，只能用tab键浏览网页内容，用户可以按照设置好的顺序去浏览网页
   * 补充说明：当设置tabindex=0时，tab访问顺序为最后一个；当设置tabindex=-1时，tab不会访问

7. title 光标浮在被设置的元素上可查看完整内容

   * 设置隐藏某一元素单行溢出文字：style="white-space:nowrap;overflow:hidden;text-overflow:ellipsis;"，以达到不换行、溢出部分省略、溢出部分用省略号表示的效果

   * 设置光标浮在被设置的元素上可查看完整内容：title="完整的内容"

     ![title 作用](title%20作用.png)

补充：CSS reset

```javascript
{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
*::before,
*::after {
  box-sizing: border-box;
}
a {
  color: inherit;
  text-decoration: none;
}
input,
button {
  font-family: inherit;
}
ol,
ul {
  list-style: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
} 
```

## 常用内容标签

1. ol+li (ordered list + list item) 有序
2. ul+li (unordered list +list item) 无序
3. dl+dt+dd (description list +term + data)
4. pre (preview)：保留空格、回车、tab效果，可更改其style为继承样式
5. hr：水平分割线
6. br (break)：换行
7. a (anchor)：超链接
8. em (emphasis)  强调 & strong 重要
9. code：默认字体等宽
10. q (quote) & blockquote

![常用内容标签效果展示](常用内容标签效果展示.png)

## 资料来源

* [饥人谷](https://xiedaimala.com/)