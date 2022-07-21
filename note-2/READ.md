# HTML 常用标签

## a标签

### a标签属性

1. href = hyper reference 超链
   
   * 永远不要以双击打开HTML来达到网页预览的目的，正确预览网页的方法如下：
     
     * 方法一：安装 http-server：yarn global add http-server，输入http-server . -c-查看网址，复制网址至浏览器，并补充完整路径
    
       ![http-server查看网址](http-server查看网址.png)
     
     * 方法二：安装 parcel：yarn global add parcel，输入parcel a-href.html
    
       ![parcel查看网址](parcel查看网址.png)
   
   * href 取值
   
     ![href测试](href测试.png)
    
     * 网址（跳转至指定网页）
       * href="https://google.com"
       * href="http://google.com"
       * href="//google.com" 优选，可协助自动跳转http或者https，避免bug
       * 补充：打开开发者工具-Network-Preserve log，点击超链接，可查看路径跳转详情
     * 路径（这里的/和./表示当前目录）
       * href="/a/b/c.html" 
       * href="a/b/c.html"
       * href="./index.html" 
       * href="index.html"
     * 伪协议（跳转并执行指定命令）
       * href="javascript:alert(1);" 点击即执行alert(1)（现下不常用）
       * href="javascript:;" 点击之后无作用（现下常用）
       * href="mailto:邮箱地址" 发邮件到该邮箱
       * href="tel:手机号" 拨打指定电话
     * id（跳转至目标锚点）
       * href="#xxx"  跳转到指定标签
      
         ![id测试](id测试.png)     

2. target 设置打开超链的位置
   * target 取值
     * target="_blank" 在空白页面打开
     * target="_self" 在当前页面打开
     * target="_top" 在顶级页面打开（有多个内嵌窗口时）
     * target="_parent" 在父级页面打开（有多个内嵌窗口时，在上一级页面打开）
   * 补充
     * window.name 在没有xxx窗口时，创建xxx窗口；在有xxx窗口时，在此窗口打开
    
       ![window.name](window.name.png)
     
     * iframe.name 理论上可以实现一个页面切换不同网页内容
    
       ![iframe.name](iframe.name.png)
   
       ![iframe.name测试](ifarme.name测试.png)

3. download 下载页面（不是所有浏览器都支持）
4. rel=noopener 增加 target=”_blank” 的安全性

### a标签作用

* 跳转至外部页面
* 跳转至内部锚点（添加id）
* 跳转至邮箱或电话（执行指定功能）等

## table标签

### table相关标签

1. thead
2. tbody
3. tfoot
4. tr（table row table里的行）
5. th（table head table里的表头）
6. td（table data table里的数据）

![table测试1](table测试1.png)

![table测试2](table测试2.png)

### table相关样式

1. table-layout 布局表格行列的算法
    * auto 布局-取决于所包含内容
    * fixed 布局-列宽等宽
2. border-collapse:collapse 相邻单元格不拥有独立边框
3. border-spacing:0 指定相邻单元格之间的边框距离为0

![table样式展示](table样式展示.png)

## img标签

### img标签作用

* 发出 get 请求（在开发者工具-method中可以看到），展示一张图片

### img标签属性

1. src source 发源地，后接路径
2. alt alter 改变，后接提示（当图片加载失败时出现）
3. width & height 每次只设置其一，另一个参数会自适应，若同时设置，会改变图片原本尺寸，导致变形

![img测试](img测试.png)

### img标签事件

onload & onerror    测试图片加载情况，可在开发者工具的console里查看

1. 加载成功时

   ![img加载成功](img加载成功.png)

2. 加载失败时，可以添加补救图片

   ![img加载失败](img加载失败.png)

### img标签响应式

max-width:100%

![img响应式](img响应式.png)

## form标签

### form标签作用

发 get 或 post 请求，然后刷新页面

### form标签属性

1. action 控制请求到哪个页面，后面接路径，如：action="/xxx" 表示get到xxx路径

   ![form-action](form-action.png)

2. method 控制用get或者post去请求，如：method="POST"（此处大写）

   ![form-method](form-method.png)

3. autocomplete 是否自动填充，用户在输入框键入内容的时，会给到内容填充选择，如：autocomplete="on"    autocomplete="off"

   ![form-autocomplete](form-autocomplete.png)

4. target 控制提交至哪个页面，如：target="_blank"  target="a"

   ![form-target](form-target.png)

### form标签事件

onsubmit 当“提交”按钮被点击时，会触发此事件，常用于表单验证

### form表单拓展

1. form 里面必须放 type=submit 才能触发 submit 事件
2. form 里input与button区别

![input&button区别](input&button区别.png)

## input标签

### input标签作用

让用户输入内容

### input标签属性

1. 类型 type：text/color/password/radio/checkbox/file/submit/hidden/button/email/number/search/tel
2. 其他 name/value/autofocus/checked/disabled/maxlength/pattern/placeholder

![input测试](input测试.png)

### input标签事件

onchange / onfocus / onblur    当用户输入改变/用户光标锁定/用户移出光标时会触发

## 其他输入标签

1. select + option 设置下拉框的内容给用户选择
2. textarea 用户可填充多行，可以设置边框固定（不允许用户自己拖拽大小）及尺寸
3. label

* 一般不监听 input 的 click 事件
* form 里面的 input 都一定要有 name（注：本节内容部分附图没写的，是错的）

## 其他有意思标签

1. video 视频
2. audio 音频
3. canvas 画画
4. svg 画矢量画

* 这些标签的兼容性一定要查看文档

## 资料来源

* [饥人谷](https://xiedaimala.com/)