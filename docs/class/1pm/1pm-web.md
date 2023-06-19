<!-- How to buil web class/1pm-web.md -->
 # HOW TO BUILD
 ### STEP1: Prepare
   Installing all the necessary tools to build the webpage:

  - [Git](https://git-scm.com/downloads); We used git to controil our version in gitlab
  - [Github](https://github.com/); We used github as a servicer for our webpage
  - [Github desktop](https://desktop.github.com/); We used github desktop to transport or push our coding from local to github
  - [VScode](https://code.visualstudio.com/); We used the visual studio code to write down our documents
  - [Nodejs](https://nodejs.org/en/); We used it to build the environment 
  - [Markdown](https://www.nexmaker.com/doc/1projectmanage/markdown.html) language; We used the Markdown language to write documents
  - [Image upload servive](https://www.nexmaker.com/doc/1projectmanage/imageuploadservice.html), We used Picgo to storage our image on cloud, in our case in gitlab and used in markdown document,
 ### STEP2: Tips
   1. Web page settings
      Build a repository, keep it Public for your team members so that anyone on the internet can have access to it and add a README file to it cause that's where you can write a long description for 
      your project.
      <br>Example
      <div class="loader"><img src="images/1.jpg" alt="#" /></div>
      <br>NOTE:Open the repository go to settings, pages under branch select the main source to enable Github pages for this repository and under folder select root and save(Attention; you selected root folder because you havn't yet installed a docs folder for this repository, therefore you will have to change this setting later)
      <br> Example
      <div class="loader"><img src="images/2.jpg" alt="#" /></div>

   2. Local settings
      Open Github desktop, clone your repository created earlier on and open it in Visual Studio Code
      <br> Example
      <div class="loader"><img src="images/3.png" alt="#" /></div>

   3. Structure
    * Add "Hello" word to the README.md save all and use github desktop to commit and push to the web page
    * We use the Docsify methode to build the structure, under the vscode menu bar open the Terminal
    <br> Example
      <div class="loader"><img src="images/4.png" alt="#" /></div>
     1. Install docsify

          "npm i docsify-cli -g"
          <br>[Read more](https://www.npmjs.com/package/docsify-build-cli)

     2. Make sure the position and then initialize environment
          
          "docsify init ./docs"
          <br>[Read more](https://cli.docsifyjs.org/#/?id=links)

     3. Preview
          
          "docsify serve docs"

     4. Browser visit http://localhost:3000
     <br> Example
      <div class="loader"><img src="images/5.png" alt="#" /></div>
     5. Setting index.html
     <br>[for more information](https://www.nexmaker.com/doc/1projectmanage/github&docsify.html)
     6. Add sidebar & navbar
     <br>[for more information](https://github.com/kn0sky/docsify-autosidebar)
     7. Write document and save all document under [VScode](https://code.visualstudio.com/)
     8. Push to Github
     <br><img src="images/push.png">

     <br>Use github desktop to push new information uploaded on VScode, Open Github under repository settings/Pages change the branch's folder from root to docs.
     <br> Example
      <div class="loader"><img src="images/6.png" alt="#" /></div>

### STEP3: Method to change Languages
#### Method 1
1. Create a folder called language and add 2 files to it(ex:en.json and cn.json)

<br>The json files should be identical in structure but different in translation as below:

<br><h1 style="font-size:1.5vw"><span style="color:black">en.json</span></h1>

{<p>"date":<span style="color:green">"Date"</span>,</p>
<p>"save":<span style="color:green">"save"</span>,</p>
<p>"cancel":<span style="color:green">"cancel"</span>,</p>}

<br><h1 style="font-size:1.5vw"><span style="color:black">cn.json</span></h1>

{<p>"date":<span style="color:green">"日期"</span>,</p>
<p>"save":<span style="color:green">"节省"</span>,</p>
<p>"cancel":<span style="color:green">"取消"</span>,</p>}
 
 <br>
 
2. Create an html page containing a sample div and put 2 links to select the language pointing to the js function listed in point 3.

<br>

```html

 <a href="#" onclick="setLanguage('en')">English</a> 
 <a href="#" onclick="setLanguage('cn')">Chinese</a>

 <div id="div1"></div>

```
3. Create 2 java script functions to get/set the selected language:

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

4. Use the variable language to populate the text.

```html

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script>

    $(document).ready(function(){
    $('#div1').text(language.date);
    });

    </script>
``` 
<br>

#### Method 2

Build your webpage using html under a docs folder.
<br><img src="images/docs1.png">

<br>After buildind, open the docs folder, copy every files and folders under it, create a new folder under the original docs folder and name it (ex:folder name"Cn" for Chinese language), past all in the new folder created (Cn), this will keep all files and folders identical in structure.

<p><br><img src="images/docs2.png"><br><img src="images/docs3.png"></p>
<br>Translate every file's contents into chinese 

### STEP4: Method for steps sidebar
Nearly all Markdown applications support the basic syntax outlined in the original Markdown design document. There are minor variations and discrepancies between Markdown processors,those are noted inline wherever possible.

<br>In our case it's as simple as <span style="background-color: #FFFF00">adding 3 pound signs(#)</span> in front of each step or phrase. Normally the number of pound signs(#) correspond to the heading level.

 ### PROBLEMS & SOLUTIONS
  1. Docsify init ./docs cannot be loaded because running scripts is disabled on this system.

      <div class="loader"><img src="images/7.jpg" alt="#" /></div>
      <br>Solution
       <br>The reason why the running scripts was disable on the system was because the running mode was strict ,you can change to Unrestricted or Bypass，by using the following code <span style="background-color: #FFFF00">Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted -Force</span> or <span style="background-color: #FFFF00">Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Bypass -Force</span>
  2. The term 'docsify' is not recognized as the name of a cmdlet, function, script file, or operable program.

      <div class="loader"><img src="images/8.jpg" alt="#" /></div>
      <br>Solution
       <br>This error means docsify cannot be found in the PATH. <span style="background-color: #FFFF00">Eitherinstall it globally</span> (recommended for many command-line tools, and where it is found in the global Github folder, already in the PATH) or <span style="background-color: #FFFF00">run it from where it is installed in the local Github</span>

     - [Verify Path](https://www.youtube.com/watch?v=pg4t48BPmh8&t=134s)
       <br><span style="background-color: #FFFF00">This PC->Properties->Advanced system settings->Environment Variables->User variables->Path->Edit</span>
       <br>Verify the path> <span style="background-color: #FFFF00">C:\Users\RAZER\Desktop\IDE\1ST YEAR\DESIGN ENGINEERING\Practice</span>
       <br>If the path is not there you can copy it and past a new path under the Edit environment variable
       <br>

  

