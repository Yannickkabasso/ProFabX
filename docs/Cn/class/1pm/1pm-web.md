<!-- How to buil web class/1pm-web.md -->
 # 如何建造
 ### 第一步：准备
   安装构建网页所需的所有工具：

  - [Git](https://git-scm.com/downloads); 我们使用git在gitlab中的版本来控制，
  - [Github](https://github.com/); 我们使用github作为我们为您网页的服务商
  - [Github 桌面](https://desktop.github.com/); 我们使用github desktop 将我们的代码从本地传输或推送到github
  - [VScode](https://code.visualstudio.com/); 我们使用visual studio code来写下我们的文档
  - [Nodejs](https://nodejs.org/en/); 我们用节点JS来搭建环境
  - [Markdown](https://www.nexmaker.com/doc/1projectmanage/markdown.html) 我们使用Markdown语言编写温度
  - [图片上传服务](https://www.nexmaker.com/doc/1projectmanage/imageuploadservice.html), 我们使用Picgo将图片存储在云端，在我们的例子中是在gitlab中，并在Markdown文档中使用
 ### 第二步: 提示
   1. 网页设置
      
      <br><br>例如
      <div class="loader"><img src="images/1.jpg" alt="#" /></div>
      <br>注意:打开存储库转到设置，分支下的页面选择主要来源以为此存储库启用Github页面，并在文件夹下选择根目录并保存（注意：您选择根文件夹是因为您尚未为此存储库安装文档文件夹，因此您稍后必须更改此设置）
      <br><br> 例如
      <div class="loader"><img src="images/2.jpg" alt="#" /></div>

   2. 本地设置
      打开Github桌面，克隆之前创建的存储库并在Visual Studio Code 中打开它
      <br><br> 例如
      <div class="loader"><img src="images/3.png" alt="#" /></div>

   3. 结构
    * 在README.md 中添加"Hello world" 字样全部保存并使用github desktop 提交并推送到网页
    * 我们使用 docsify 方法构建结构，在Vscode 菜单栏下打开 Terminal
    <br><br> 例如
      <div class="loader"><img src="images/4.png" alt="#" /></div>
     1. 安装文档（docsify）

          "npm i docsify-cli -g"
          <br>[了解](https://www.npmjs.com/package/docsify-build-cli)

     2. 确定位置然后初始化环境
          
          "docsify init ./docs"
          <br>[了解](https://cli.docsifyjs.org/#/?id=links)

     3. 预习
          
          "docsify serve docs"

     4. 浏览器访问 http://localhost:3000
     <br><br>例如
      <div class="loader"><img src="images/5.png" alt="#" /></div>
     5. 设置 index.html
     <br>[了解跟多信息](https://www.nexmaker.com/doc/1projectmanage/github&docsify.html)
     6. 添加侧边栏和导航栏
     <br>[了解跟多信息](https://github.com/kn0sky/docsify-autosidebar)
     7. [VScode](https://code.visualstudio.com/)下写文档并保存所有文档
     8. 推送到Github
     <br>使用 github desktop 推送新资料上传到 VScode, 打开 Github 在 repository settings/Pages 下将分支的文件夹从 root 改为 docs.
     <br><br> 例如
      <div class="loader"><img src="images/push.png" alt="#" /></div>
     <br>

### 第三步: 更改语言的方法
#### 方法一
1. 创建一个名为语言的文件夹并向其中添加 2 个文件(例如:en.json 和 cn.json)

<br>json 文件的结构应该相同，但翻译不同，如下所示 :

<br><h1 style="font-size:1.5vw"><span style="color:black">en.json</span></h1>

{<p>"date":<span style="color:green">"Date"</span>,</p>
<p>"save":<span style="color:green">"save"</span>,</p>
<p>"cancel":<span style="color:green">"cancel"</span>,</p>}

<br><h1 style="font-size:1.5vw"><span style="color:black">cn.json</span></h1>

{<p>"date":<span style="color:green">"日期"</span>,</p>
<p>"save":<span style="color:green">"节省"</span>,</p>
<p>"cancel":<span style="color:green">"取消"</span>,</p>}
 
 <br><br>
 
2. 创建一个包含示例div的html页面，并放置第三点中列出的2个链接函数.

<br>

```html

 <a href="#" onclick="setLanguage('en')">English</a> 
 <a href="#" onclick="setLanguage('cn')">Chinese</a>

 <div id="div1"></div>

```
3. 创建 2 javaScript 函数来获取/设置所选语言 :

```htm 

<script>
var language; 
function getLanguage() {
(localStorage.getItem('language') == null) ? setLanguage('en') : false;
$.ajax({ 
url:  '/language/' +  localStorage.getItem('language') + '.json', 
dataType: 'json', async: false, dataType: 'json', 
success: function (lang) { language = lang } });
}
function setLanguage(lang) {
localStorage.setItem('language', lang);
}
</script>

```
<br>

4. 使用可变语言填充文本.

```html

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script>

    $(document).ready(function(){
    $('#div1').text(language.date);
    });

    </script>
``` 
<br>

#### 方法二

使用 docs 文件夹下的 html 构建您的网页.
<br><img src="images/docs1.png">

<br> 创造之后，打开 docs 文件夹，复制它下面的所有文件和文件夹，在原来的 docs 文件夹下新建一个文件夹并命名（例如：文件夹名称为中文“C你”），粘贴所有的新创建的文件（Cn)， 
这将使所有文件和文件夹在结构上保持相同。
<p><br><img src="images/docs2.png"><br><img src="images/docs3.png"></p>
<br> 将每个文件的内容翻译成中文

### 第四步：步骤侧边栏的方法
几乎所有 Markdown 应用程序都支持原始 Markdown 设计文档中概述的基本语法. Markdown 处理器之间存在细微的差导，这些差导和会尽可能内联标注.

<br>在我们的例子中，它就像在每个步骤或短语前<span style="background-color: #FFFF00">添加 3 (#) 一样简单。通常，井号 (#) 的数量对应于标题级别</span>.


 ### 问题与解决方案
  1. 无法加载 Docsify init ./docs，因为在此系统上禁用运行脚本.

      <div class="loader"><img src="images/7.jpg" alt="#" /></div>
      <br>解决方案
       <br> 系统运行脚本被禁用的原因是因为运行模式是严格的，您可以通过以下代码更改为 Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted -Force or Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Bypass -Force
  2. 术语“docsify”未被识别为 cmdlet、函数、脚本文件或可运行程序的名称.

      <div class="loader"><img src="images/8.jpg" alt="#" /></div>
      <br>解决方案
       <br> 此错误意味着在 PATH 中找不到 docsify。要么全局安装它（推荐用于许多命令行工具，它位于全局 Github 文件夹中，已经在 PATH 中），要么从它在本地 Github 中的安装位置运行它

     - [验证路径](https://www.youtube.com/watch?v=pg4t48BPmh8&t=134s)
       <br>此PC->属性->高级系统设置->环境变量->用户变量->路径->编辑
       <br>验证路径 > C:\Users\RAZER\Desktop\IDE\1ST YEAR\DESIGN ENGINEERING\Practice
       <br>如果路径不存在，您可以复制它并在 Edit 环境变量下通过一个新路径
       <br>

  

