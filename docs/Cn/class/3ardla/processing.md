<!-- Processing/processing.md -->
<h1 style="font-size:2vw"><span style="color:black">PROCESSING 编程语言</span></h1>
<h1 style="font-size:1.5vw"><span style="color:black">简介</span></h1>
<br>

[Processing 编程语言](https://processing.org/download) 是一个灵活的软件草图本和一种在视觉艺术背景下学习编码的语言。自 2001 年以来，Processing 在视觉艺术领域推广软件素养，并在技术领域推广视觉素养。有成千上万的学生、艺术家、设计师、研究人员和爱好者使用 Processing 进行学习和原型制作。<br>Processing 编程语言是一个免费的图形库和集成开发环境（IDE），旨在为电子艺术、新媒体艺术和视觉设计社区提供帮助，并通过可视化编程的方式教授非程序员计算机编程的基础知识。

<br>Processing 编程语言使用Java语言，提供了额外的简化，如额外的类和别名数学函数和操作。它还提供了一个图形用户界面，简化了编译和执行阶段。

<br>Processing语言和IDE是其他项目的先驱，包括Arduino和Wiring。

- [下载软件](https://processing.org/download)

<h1 style="font-size:1.5vw"><span style="color:black">相似的软件</span></h1>

[Processing.js](https://www.tutorialspoint.com/online_processingjs_editor.php)
<br>Processing.js是一个开源编程语言，是processing可视化语言的移植版本，为那些想要在Web上编写图像、动画和交互而不使用Flash或Java小程序的人们提供了方便。
<br>

[Vvvv](https://www.visualprogramming.net/)
<br>vvv是一个图形化的编程环境，用于简化原型设计和开发。它被设计用于处理具有物理接口、实时动态图形、音频和视频的大型媒体环境，可以与多个用户同时交互。
<br>

[开放框架](https://openframeworks.cc/download/)
<br>开放框架(openFrameworks)是一个开源的C++工具包，旨在通过提供简单直观的实验框架来协助创意过程。

<h1 style="font-size:1.2vw"><span style="color:black">参考</span></h1>

- [Nexmaker](https://www.nexmaker.com/doc/10Interface-application-programming/processing.html)
- [学习Processing编程语言](https://www.amazon.com/gp/product/0123944430/ref=as_li_ss_tl?ref_=nav_ya_signin&linkCode=sl1&tag=processing09-20&linkId=fb0eeedd8fb1016a790e83d538a1c030)


<h1 style="font-size:1.5vw"><span style="color:black">Processing 编程语言 Demo</span></h1>
<h1 style="font-size:1vw"><span style="color:black">鼠标交互</span>: Reach</h1>

机械臂通过计算角度来跟随鼠标的位置： [atan2()](https://processing.org/reference/atan2_.html).
<div class="loader"><img src="images/mouse.gif" alt="mouse.gif"max-width="800" height="500" />

<h1 style="font-size:1vw"><span style="color:black">代码</span></h1>


```html
/**
 * Reach 2  
 * based on code from Keith Peters.
 * 
 * The arm follows the position of the mouse by
 * calculating the angles with atan2(). 
 */

int numSegments = 10;
float[] x = new float[numSegments];
float[] y = new float[numSegments];
float[] angle = new float[numSegments];
float segLength = 26;
float targetX, targetY;

void setup() {
  size(640, 360);
  strokeWeight(20.0);
  stroke(255, 100);
  x[x.length-1] = width/2;     // Set base x-coordinate
  y[x.length-1] = height;  // Set base y-coordinate
}

void draw() {
  background(0);
  
  reachSegment(0, mouseX, mouseY);
  for(int i=1; i<numSegments; i++) {
    reachSegment(i, targetX, targetY);
  }
  for(int i=x.length-1; i>=1; i--) {
    positionSegment(i, i-1);  
  } 
  for(int i=0; i<x.length; i++) {
    segment(x[i], y[i], angle[i], (i+1)*2); 
  }
}

void positionSegment(int a, int b) {
  x[b] = x[a] + cos(angle[a]) * segLength;
  y[b] = y[a] + sin(angle[a]) * segLength; 
}

void reachSegment(int i, float xin, float yin) {
  float dx = xin - x[i];
  float dy = yin - y[i];
  angle[i] = atan2(dy, dx);  
  targetX = xin - cos(angle[i]) * segLength;
  targetY = yin - sin(angle[i]) * segLength;
}

void segment(float x, float y, float a, float sw) {
  strokeWeight(sw);
  pushMatrix();
  translate(x, y);
  rotate(a);
  line(0, 0, segLength, 0);
  popMatrix();
}
```

- [代码](https://processing.org/examples/reach2.html)

<h1 style="font-size:1vw"><span style="color:black">键盘交互</span>: 贪吃蛇游戏</h1>
这是一个简单的贪吃蛇游戏，也是在Processing中创建小游戏的一个测试。
<div class="loader"><img src="images/snakegame.gif" alt="snakegame.gif"max-width="800" height="500" />
<h1 style="font-size:1vw"><span style="color:black">代码</span></h1>

```html


//BY Ian151 (ChromeWing)
//inspired by the original snake game
//this is a test for creating small games in processing.

int angle=0;
int snakesize=5;
int time=0;
int[] headx= new int[2500];
int[] heady= new int[2500];
int applex=(round(random(47))+1)*8;
int appley=(round(random(47))+1)*8;
boolean redo=true;
boolean stopgame=false;
void setup()
{
  restart();
  size(400,400);
  textAlign(CENTER);
}
void draw()
{
  if (stopgame)
  {
    //do nothing because of game over (stop playing)
  }
  else
  {
    //draw stationary stuff
  time+=1;
  fill(255,0,0);
  stroke(0);
  rect(applex,appley,8,8);
  fill(0);
  stroke(0);
  rect(0,0,width,8);
  rect(0,height-8,width,8);
  rect(0,0,8,height);
  rect(width-8,0,8,height);
  //my modulating time by 5, we create artificial frames each 5 frames
  //(otherwise the game would go WAY too fast!)
  if ((time % 5)==0)
  {
    travel();
    display();
    checkdead();
  }
  }
}
//controls:
void keyPressed()
{
  if (key == CODED)
  {
    //what key was pressed? is the previous angle the opposite direction?
    //we wouldn't want to go backwards into our body, that would hurt!
    //also, is the previous body segment in front of the direction? 
    //(based on the previous question, but added for secure turning without suicide)
    if (keyCode == UP && angle!=270 && (heady[1]-8)!=heady[2])
    {
      angle=90;
    }
    if (keyCode == DOWN && angle!=90 && (heady[1]+8)!=heady[2])
    {
      angle=270;
    }if (keyCode == LEFT && angle!=0 && (headx[1]-8)!=headx[2])
    {
      angle=180;
    }if (keyCode == RIGHT && angle!=180 && (headx[1]+8)!=headx[2])
    {
      angle=0;
    }
    if (keyCode == SHIFT)
    {
      //restart the game by pressing shift
      restart();
    }
  }
}
void travel()
{
  for(int i=snakesize;i>0;i--)
  {
    if (i!=1)
    {
      //shift all the coordinates back one array
      headx[i]=headx[i-1];
      heady[i]=heady[i-1];
    }
    else
    {
      //move the new spot for the head of the snake, which is
      //always at headx[1] and heady[1].
      switch(angle)
      {
        case 0:
        headx[1]+=8;
        break;
        case 90:
        heady[1]-=8;
        break;
        case 180:
        headx[1]-=8;
        break;
        case 270:
        heady[1]+=8;
        break;
      }
    }
  }
  
}
void display()
{
  //is the head of the snake eating the apple?
  if (headx[1]==applex && heady[1]==appley)
  {
    //grow and spawn the apple somewhere away from the snake
    //(currently some of the code below might not be working, but the game still works.)
    snakesize+=round(random(3)+1);
    redo=true;
    while(redo)
    {
      applex=(round(random(47))+1)*8;
      appley=(round(random(47))+1)*8;
      for(int i=1;i<snakesize;i++)
      {
        
        if (applex==headx[i] && appley==heady[i])
        {
          redo=true;
        }
        else
        {
          redo=false;
          i=1000;
        }
      }
    }
  }
  //draw the new head of the snake...
  stroke(sinecolor(1),sinecolor(0),sinecolor(.5));
  fill(0);
  rect(headx[1],heady[1],8,8);
  //...then erase the back end of the snake.
  fill(255);
  rect(headx[snakesize],heady[snakesize],8,8);
  
}
void checkdead()
{
  for(int i=2;i<=snakesize;i++)
  {
    //is the head of the snake occupying the same spot as any of the snake chunks?
    if (headx[1]==headx[i] && heady[1]==heady[i])
    {
      fill(255);
      rect(125,125,160,100);
      fill(0);
      text("GAME OVER",200,150);
      text("Score:  "+str(snakesize-1)+" units long",200,175);
      text("To restart, press Shift.",200,200);
      stopgame=true;
    }
    //is the head of the snake hitting the walls?
    if (headx[1]>=(width-8) || heady[1]>=(height-8) || headx[1]<=0 || heady[1]<=0)
    {
      fill(255);
      rect(125,125,160,100);
      fill(0);
      text("GAME OVER",200,150);
      text("Score:  "+str(snakesize-1)+" units long",200,175);
      text("To restart, press Shift.",200,200);
      stopgame=true;
    }
  }
}
void restart()
{
  //by pressing shift, all of the main variables reset to their defaults.
  background(255);
  headx[1]=200;
  heady[1]=200;
  for(int i=2;i<1000;i++)
  {
    headx[i]=0;
    heady[i]=0;
  }
  stopgame=false;
  applex=(round(random(47))+1)*8;
  appley=(round(random(47))+1)*8;
  snakesize=5;
  time=0;
  angle=0;
  redo=true;
}
float sinecolor(float percent)
{
  float slime=(sin(radians((((time +(255*percent)) % 255)/255)*360)))*255;
  return slime;
}

```

- [参考e](https://openprocessing.org/sketch/50988/#)