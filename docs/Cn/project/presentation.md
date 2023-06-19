<!-- project/presentation.md -->
# 太阳能板跟踪能量

<br>
我们的最终目标是建立一个自动跟踪太阳能的能量系统，旨在尽可能捕获太阳光作为辐射能源，并将其转换为直流电。该项目基于LDR传感器，我们制作了可旋转的太阳能系统，系统在夜间有固定的初始位置，但当有阳光照射时，太阳能系统会通过感应到光线的存在自动唤醒，所有太阳能电池板会逆时针旋转并像向日葵一样打开跟随太阳的旋转，太阳落山后所有太阳能电池板会自动顺时针旋转并回到初始位置，以便于接收第二天的阳光。
<br>
<br>
我们的太阳能板跟踪能量技术用于将太阳能收集器、反射器或光伏板定向朝向太阳。随着太阳在天空中的移动，跟踪装置确保太阳能收集器自动跟随并保持最佳角度以接收最多的太阳辐射。

<h1 style="font-size:1.5vw"><span style="color:black">I. 所需材料</span></h1>

<link rel="stylesheet" href="css/bootstrap-grid.min.css"/>
<div class="demo">
        <div class="container">
            <div class="row text-center">
                <h1 class="white"></h1>
            </div>

<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/solar.jpg">
                        <div class="team-content">
                            <h3 class="title">太阳能电池板（6块，每块6伏特）</h3>
                        </div>
                    </div>
                </div>

<div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/battery.jpg">
                        <div class="team-content">
                            <h3 class="title">12伏锂离子电池</h3>
                        </div>
                    </div>
                </div>

<div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/nano.jpg">
                        <div class="team-content">
                            <h3 class="title">Arduino Nano V3开发板</h3>
                        </div>
                    </div>
                </div>
                 <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/l293d.jpg">
                        <div class="team-content">
                            <h3 class="title">L293D IC驱动器 + IC底座</h3>
                         </div>
                     </div>
                 </div>

<div class="row">
                     <div class="col-md-4 col-sm-6">
                         <div class="our-team">
                                 <img src="images/regulator.jpg">
                             <div class="team-content">
                                 <h3 class="title">7806稳压器</h3>
                        </div>
                    </div>
                </div>


<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/resistor.jpg">
                        <div class="team-content">
                            <h3 class="title">10k碳膜电阻</h3>
                        </div>
                    </div>
                </div>
                <div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/ldr.jpg">
                        <div class="team-content">
                            <h3 class="title">光敏电阻 (LDRs)</h3>
                        </div>
                    </div>
                </div>
                <div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/servo.jpg">
                        <div class="team-content">
                            <h3 class="title">舵机</h3>
                        </div>
                    </div>
                </div>
<div class="row">
                 <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/gear.jpg">
                        <div class="team-content">
                            <h3 class="title">N20齿轮电机</h3>
                         </div>
                     </div>
                 </div>
                <div class="row">
                     <div class="col-md-4 col-sm-6">
                         <div class="our-team">
                                 <img src="images/header.jpg">
                             <div class="team-content">
                                 <h3 class="title">公头和母头排针</h3>
                        </div>
                    </div>
                </div>

<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/pcb.jpg">
                        <div class="team-content">
                            <h3 class="title">印刷电路板 (PCB)</h3>
                        </div>
                    </div>
                </div>

<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/switch.jpg">
                        <div class="team-content">
                            <h3 class="title">限位开关</h3>
                        </div>
                    </div>
                </div>
</div>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">II. 使用的软件</span></h1>

<a href="https://www.arduino.cc/en/software" class="fab fa-facebook"><span style="font-size:1.2vw">Arduino IDE开发环境</span></a>
<br>
<br><a href="https://easyeda.com/" class="fab fa-facebook"><span style="font-size:1.2vw">EasyEDA电路设计软件</span></a>
<br><br><a href="https://www.autodesk.com/products/fusion-360/free-trial" class="fab fa-facebook"><span style="font-size:1.2vw">Fusion 360</span></a>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">III. Fusion 360零件设计软件</span></h1>

<br>

<img src="images/fusion.jpg" alt="fusion.jpg" max-width="1200" height="800">

<br>
<h1 style="font-size:1.5vw"><span style="color:black">IV. 如何制作</span></h1>

<br>
我们首先购买了材料并打印了3D零件。 
<br>

<img src="images/allparts.jpg" alt="allparts.jpg" max-width="1200" height="800">

<br>在我们使用 Easyeda 设计原理图并制作了自定义 PCB 后，请翻译成中文。
<br><div class="loader"><img src="images/pcb.png" alt="#" /></div>
<br><div class="loader"><img src="images/pcb1.jpg" alt="#" /></div>

<br><br>
现在，在我们尝试使用自定义 PCB 之前，我们需要编译并上传代码到 Arduino Nano。此项目的代码可以在这里找到。

```html

#include <Servo.h> 

Servo horizontal; // horizontal servo
int servoh = 180; 
int servohLimitHigh = 175;
int servohLimitLow = 5;
// 65 degrees MAX

Servo vertical; // vertical servo
int servov = 0; 
int servovLimitHigh = 60;
int servovLimitLow = 0;

// LDR pin connections
// name = analogpin;
int ldrlt = A1; //LDR top left - BOTTOM LEFT <--- BDG
int ldrrt = A2; //LDR top rigt - BOTTOM RIGHT
int ldrld = A3; //LDR down left - TOP LEFT
int ldrrd = A4; //ldr down rigt - TOP RIGHT
int ldrmt = A5;

const int button1 = 9;
const int button2 = 10; 
const int motorA =  7;
const int motorB =  8;
int buttonStateA = 0; 
int buttonStateB = 0; 

  int pos = 0;
  int pos2 = 0;
  int oldvalue;
  int oldvalue2;
  

void setup(){
  
horizontal.attach(5);
vertical.attach(6);
horizontal.write(180);
vertical.write(0);
  pinMode(motorA, OUTPUT);
  pinMode(motorB, OUTPUT);
  pinMode(button1, INPUT);
  pinMode(button1, INPUT);
delay(2500);
}
void loop() {
  int ldrStatus = analogRead(ldrmt);
  if (ldrStatus >30) {
    buttonStateA = digitalRead(button1);
     if (buttonStateA == LOW) {
    
    digitalWrite(motorA, HIGH); //COUNTER clockwise
    digitalWrite(motorB, LOW);
  }else{digitalWrite(motorA, LOW);
    digitalWrite(motorB, LOW);
    }

int lt = analogRead(ldrlt); // top left
int rt = analogRead(ldrrt); // top right
int ld = analogRead(ldrld); // down left
int rd = analogRead(ldrrd); // down right
int dtime = 10; int tol = 90; // dtime=diffirence time, tol=toleransi
int avt = (lt + rt) / 2; // average value top
int avd = (ld + rd) / 2; // average value down
int avl = (lt + ld) / 2; // average value left
int avr = (rt + rd) / 2; // average value right
int dvert = avt - avd; // check the diffirence of up and down
int dhoriz = avl - avr;// check the diffirence og left and rigt

//if(lt>90){
//if(Switch_a==LOW){
 // digitalWrite(9==HIGH);
// digitalWrite(10==LOW);
 // delay(1000);
//}}

if (-1*tol > dvert || dvert > tol) 
 {
 if (avt > avd)
 {
 servov = ++servov;
 if (servov > servovLimitHigh)
 {servov = servovLimitHigh;}
 }
 else if (avt < avd)
 {servov= --servov;
 if (servov < servovLimitLow)
 { servov = servovLimitLow;}
 }
 vertical.write(servov);
 }
if (-1*tol > dhoriz || dhoriz > tol) // check if the diffirence is in the tolerance else change horizontal angle
 {
 if (avl > avr)
 {
 servoh = --servoh;
 if (servoh < servohLimitLow)
 {
 servoh = servohLimitLow;
 }
 }
 else if (avl < avr)
 {
 servoh = ++servoh;
 if (servoh > servohLimitHigh)
 {
 servoh = servohLimitHigh;
 }
 }
 else if (avl = avr)
 {
 delay(10);
 }
 horizontal.write(servoh);
 }
  
 delay(dtime);
  

  }

else{
  oldvalue = horizontal.read();
  oldvalue2 = vertical.read();
  
 for (pos = oldvalue; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    horizontal.write(pos);
    delay(15);
 }
    for (pos2 = oldvalue2; pos2 <= 0; pos2 += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    
vertical.write(pos2);           // tell servo to go to position in variable 'pos'
    delay(15);}
    buttonStateB = digitalRead(button2);
    if (buttonStateB == LOW) {
    
    digitalWrite(motorA, LOW); //clockwise
    digitalWrite(motorB, HIGH);
  }else{digitalWrite(motorA, LOW);
    digitalWrite(motorB, LOW);
    }}}
```

<br><div class="loader"><img src="images/pcb2.jpg" alt="#" /></div>
<br><br>

然后，我们创建了 Gerber 文件并从 XXX 订购了自定义 PCB。 [NEXTPCB](https://passport.hqonline.com/register?reurl=https%3A%2F%2Fwww.nextpcb.com%2Fregister%3Fcode%3Dtechboysxwd)

<br><div class="loader"><img src="images/nextpcb.jpg" alt="#" /></div>
<br><div class="loader"><img src="images/pcbf.jpg" alt="#" /></div>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">太阳能电池板连接 </span></h1>
<br><div class="loader"><img src="images/solar panel.jpg" alt="#" /></div>
<br> 
<br> 我们将使用 6 片太阳能电池板，每个电池板输出功率为 6V 70mAh。我们将把一对电池板串联起来，然后将 3 对电池板并联起来，这样电压输出将为 6+6=12V。因此，基本上当电池板完全展开时，电压输出为 12V，当电池板进入家庭位置时，电压输出将为 1-3 伏特。
<br><div class="loader"><img src="images/solars.jpg" alt="#" /></div>
<br><div class="loader"><img src="images/solarm.jpg" alt="#" /></div>
<br><div class="loader"><img src="images/solaro.jpg" alt="#" /></div>
<br>
<br> 
<h1 style="font-size:1.2vw"><span style="color:black">LDR（光敏电阻）及其工作原理</span></h1>
<br>LDR（光敏电阻）是一种光电阻，其电阻值随着光线强度的增加而降低。LDR 或光敏电阻是由一种半导体材料制成，其电阻值较高。这是因为有非常少的电子是自由的并且能够移动 - 绝大部分的电子被锁定在晶格中，无法移动。因此，在这种状态下，LDR 的电阻较高。
<br>当光照射在半导体上时，光子被半导体晶格吸收，其中一部分能量转移到电子上。这使得其中一部分电子具有足够的能量从晶格中脱离出来，从而能够导电。这导致半导体的电阻降低，因此整个 LDR 的电阻也会降低。这个过程是逐渐进行的，当更多的光照在 LDR 半导体上时，更多的电子被释放来导电，电阻进一步降低。
<br><div class="loader"><img src="images/solarl.jpg" alt="#" /></div>
<br>您可以看到，第五个电阻器放置在太阳能电池板的中间位置。当光线最弱时，微控制器 Arduino 读取电阻值并在代码部分设置阈值。当有光线可用并且阈值被突破时，Arduino 通过 L293D 驱动器逆时针旋转 N20 齿轮电机，直到限位开关触发为止。当逆时针限位开关被按下时，电池板停止旋转，并处于完全打开的位置。当按下按钮后，主要工作将进行。根据太阳的旋转，其他四个 LDR 感应光线并将数据发送到 Arduino，然后 Arduino 处理数据，旋转舵机以使其按照太阳的旋转方向旋转。舵机的旋转位置最大为 170 度。当太阳下山时，第五个 LDR 再次感应数据，此时过程是相反的。LDR 数据降到阈值以下时，Arduino 将顺时针旋转 N20 电机，直到第二个限位开关按下，并将舵机运行到初始位置。第二天有光线时，相同的过程将再次进行。
<br>
<h1 style="font-size:1.5vw"><span style="color:black">项目电路</span></h1>  
<br><div class="loader"><img src="images/solara.jpg" alt="#" /></div>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">试验</span></h1>  
<br><br>
<img src="images/trial1.gif" alt="trial1.gif" max-width="1000" height="700">
<br><br>
<img src="images/trial1.gif" alt="trial2.gif" max-width="1000" height="700">
<br><br>
<img src="images/trial1.gif" alt="trial3.gif" max-width="1000" height="700">
<br>
<br>
<br><h1 style="font-size:1.5vw"><span style="color:black">最终设计带有功率和电流显示（电压=11.14V，电流=445mA，功率=4.978W）</span></h1> 
<br><div class="loader"><img src="images/display.jpg" alt="#" /></div>
<br><br><div class="loader"><img src="images/displayp.jpg" alt="#" /></div>
<br><br><div class="loader"><img src="images/displaypo.jpg" alt="#" /></div>
<br>
<h1 style="font-size:1.5vw"><span style="color:black">Demo</span></h1> 
<br><br>
<img src="images/demo.gif" alt="demo.gif" max-width="1000" height="700">

<br>
<h1 style="font-size:1.5vw"><span style="color:black">创新</span></h1>
我们的太阳能板跟踪能源系统有6个太阳能板，旋转90度角度，比固定的太阳能板产生更多的能源，增加了40%的能源输出量。该系统采用双轴跟踪系统，能够始终面向太阳，生产效率最高可提高10%。它们的抬高式设计还允许太阳能板自然冷却，提高了其效率。

<br>
<br>
<h1 style="font-size:1.5vw"><span style="color:black">太阳能花市场 - 全球行业分析和预测（2022年至2029年）</span></h1>
<br>全球太阳能花市场在2022年的市值为1400万美元，并预计在2028年达到3920万美元，年复合增长率（CAGR）在2023年至2028年间为16.00％。

<br>
主要优点：太阳能花是一种地面安装的全一体化太阳能系统，带有跟踪器，可跟随太阳。它利用先进的自动化技术快速监测太阳，比传统静态太阳能电池板多产生高达40％的能量。
<br>同时，太阳花具有自清洁的独特功能。对于利用太阳能的认知的提高和对可持续能源的鼓励的优点的增加是推动全球太阳花市场的主要因素。
<br>然而，高额的初始投资和缺乏技术专业人员是制约全球太阳能花市场的主要因素。
<br>
<h1 style="font-size:1vw"><span style="color:black">顶尖影响因素</span></h1>
执行严格的规定以促进环境保护，增加了能源行业转向清洁环保的能源资源。此外，由于技术进步，太阳能发电的价格预计将在未来几年内降低。

<br>
<h1 style="font-size:1vw"><span style="color:black">市场趋势</span></h1>
● 对环境的认识和使用可再生资源进行能源发电的过程
<br>● 随着人们对多种非可再生资源的碳排放意识的提高以及燃料价格的上涨，预计太阳能花市场将迎来需求激增。
<br>● 有利的政府政策和优先考虑因素是市场增长的关键驱动因素。
<br>● 技术进步和太阳能领域研发计划的增加是市场增长的积极因素。
<br>● 对环保能源需求的增加以及太阳能发电技术领域的进步对太阳能花市场产生了积极影响。

<br>
<h1 style="font-size:1vw"><span style="color:black">太阳花市场细分分析:</span></h1>

<br>太阳花市场被划分为: 
<br>连通性（并网和离网）
<br>离网部分预计在整个预测期间以更快的复合年增长率扩大。
<br>应用领域（住宅区，学校和大学，娱乐公园，山区和其他）
<br>学校和大学领域预计将以更快的速度增长，这是因为在欧洲和美国广泛实施太阳花的规模较大。
<br>区域 (北美洲、欧洲、亚太地区、中东和非洲、拉丁美洲)
<br>北美洲预计将是太阳花市场的主导地区。在未来几年里，太阳能实施支出的增加是估计将增加该地区市场的主要因素。美国在2021年影响了北美太阳花市场。
<br>2021年7月，弗吉尼亚韦斯利大学成为全国首批采用智能太阳花的高等教育机构之一。亚太地区是全球太阳花市场的另一个主要地区。


<h1 style="font-size:1.5vw"><span style="color:black">关键技术分析</span></h1>
<h1 style="font-size:1vw"><span style="color:black">*01 光伏电池（太阳能光伏电池） </span></h1>
<br><div class="loader"><img src="images/solar-photovoltaic-pv.jpeg" alt="#" /></div>
<br>2021年，太阳能光伏发电量创纪录增长了179 TWh（增长22％），超过1,000 TWh。它展示了所有可再生能源技术中第二大的绝对发电增长，仅次于风能。在世界大部分地区，太阳能光伏正在成为新电力发电的最低成本选择，预计未来几年将推动投资增长。然而，为实现2050年净零排放目标，2022-2030年期间需要平均年发电增长率为25％。这相当于年容量部署增加三倍以上，需要更大的政策雄心和公共和私营利益相关者的更多努力，特别是在电网整合和缓解政策、监管和融资挑战方面。这在新兴和发展中国家尤其如此。

<br>
<h1 style="font-size:1vw"><span style="color:black">*02 Arduino Nano v3</span></h1>
<br><div class="loader"><img src="images/v3.webp" alt="#" /></div>
<br>Arduino Nano是一款基于ATmega328（Arduino Nano 3.x）的小型、完整和面包板友好型的板子。它的功能基本上与Arduino Duemilanove相同，但外形不同。它只缺少一个直流电源插孔，使用Mini-B USB电缆而不是标准电缆。Arduino Nano可以通过Mini-B USB连接、6-20V未调整的外部电源（引脚30）或5V调整的外部电源（引脚27）供电。电源会自动选择最高电压源。
<br>Nano上的每个数字引脚都可以使用pinMode()、digitalWrite()和digitalRead()函数作为输入或输出。它们的工作电压为5伏特。每个引脚可以提供或接收最大40毫安的电流，并具有20-50千欧姆的内部上拉电阻（默认情况下断开连接）。此外，一些引脚具有特殊的功能：
<br>

* 串口：0（RX）和1（TX）。用于接收（RX）和发送（TX）TTL串行数据。这些引脚连接到FTDI USB到TTL串行芯片的相应引脚。
* 外部中断：2和3。这些引脚可以配置为在低电平、上升或下降沿或值变化时触发中断。有关详细信息，请参见attachInterrupt（）函数。
* PWM：3、5、6、9、10和11。使用analogWrite（）函数提供8位PWM输出。
* SPI：10（SS）、11（MOSI）、12（MISO）、13（SCK）。这些引脚支持SPI通信，尽管由底层硬件提供，但目前未包含在Arduino语言中。
* LED：13。有一个内置LED连接到数字引脚13。当引脚处于高电平时，LED亮起；当引脚处于低电平时，LED关闭。
<br>Nano板有8个模拟输入引脚，每个引脚提供10位分辨率（即1024个不同的值）。默认情况下，它们从地到5伏特进行测量，但是可以使用analogReference()函数更改它们范围的上限。模拟引脚6和7不能用作数字引脚。此外，一些引脚具有专用功能：
<br>
* I2C：A4（SDA）和A5（SCL）。使用Wire库支持I2C（TWI）通信（Wiring网站上有文档）。
<br>
这块板子上还有其他几个引脚:

* AREF。模拟输入的参考电压，与 analogReference() 一起使用。
* 复位。将此线路拉低以重置微控制器。通常用于为屏蔽板添加复位按钮，以避免阻挡板上的按钮。
<h1 style="font-size:1vw"><span style="color:black">*03 L293D IC 驱动芯片</span></h1>
<br><div class="loader"><img src="images/L293D.webp" alt="#" /></div>
<br>L293D是一种双通道H桥电机驱动器，能够驱动一对直流电机或单个步进电机。这意味着它可以单独驱动两个电机，同时也是通过Arduino板控制直流电机最便宜、最简单的方式之一，这使得它非常适合用于构建这个项目。

<br>L293D通常用于驱动电机，但也可以用于驱动任何感性负载，例如继电器线圈或大型开关功率晶体管。它能够驱动四个线圈，四个单向直流电机，两个双向直流电机或一个步进电机。
<br>
<h1 style="font-size:1vw"><span style="color:black">*04 PCB</span></h1>
<br><div class="loader"><img src="images/npcb.jpg" alt="#" /></div>
<br>电气和电子领域的一个关键概念是印刷电路板(PCB)。它允许元件以安全和可控的方式相互连接。 PCB是一种具有线路和焊盘的板子，它将各个点连接在一起，也允许信号和电源在物理设备之间进行路由。
<br>电子元件可以通过焊接的方式固定在外层的导电垫上，形状设计成可接受元件端子的形式，以电气连接和机械固定它们。

<br>
<h1 style="font-size:1.5vw"><span style="color:black">我们的项目与联合国可持续发展目标（SDGs） </span></h1>
<br>
联合国通过了17个可持续发展目标，旨在改善全球人民的生活条件。
<br>可持续发展目标是对所有国家的行动呼吁——包括贫穷、富裕和中等收入国家——以促进繁荣和更好的生活质量，同时保护地球。它们认识到，消除贫困和其他剥夺必须与建立经济增长和解决一系列社会需求（包括社会保障、卫生、教育、就业机会和减少不平等），并应对气候变化和环境保护的策略相结合。


<br>我们的项目（太阳能面板，电源系统）符合联合国可持续发展目标中的一些。众所周知，电力是日常生活中不可或缺的一部分，电力的发电标志着生产力的进一步解放。电力系统指完成电能的发电、变换、输送和配电的过程。随着科技的快速变革，电力技术也取得了巨大的进步，人类也进入了电气信息时代。只有一个可靠、安全和负担得起的电力供应和分配系统才能确保正常的工作和生活环境。信息技术和其他高新技术都是建立在电力应用基础上的，电能在现代工业生产和社会生活中占据着非常重要的地位。

<br>我们的项目包括三个可持续发展目标（SDGs）:

* SDG目标7: 负担得起的清洁能源
* SDG目标11: 可持续城市和社区
* SDG目标13: 气候行动


<br>联合国大会的开放工作组提出的可持续发展目标（SDGs）认识到自然环境及其资源对人类福祉的重要性。总体上，它绝对是21世纪一个值得拥有的宪章，因为它应对了我们作为全球社会所面临的各种挑战。SDG 7 - “确保所有人可获得负担得起、可靠、可持续和现代的能源” - 是每个国家都面临的挑战，触及每个人。为了理解实现这一目标的必要性以及所需的措施，我们应该详细解释目标本身的声明。SDG 7的四个维度是负担能力、可靠性、可持续性和现代化。这些不同的维度并不是相互独立的，它们重叠，在某些情况下甚至相互包含。

<br>在考虑能够获得经济实惠的能源时，需要考虑能源使用的异质性。世界各地的能源利用情况很大程度上取决于不同的自然资源储量和购买力。例如，一个拥有大量煤炭储量的国家很可能会广泛使用这种资源来实现经济工业化。这个国家的居民很可能会将其作为主要的发电手段。
<br>另一方面，生活在没有现成化石燃料储备的地方的人们可能依赖更为原始的燃烧方法，如木纤维或甚至动物粪便。事实上，这是人类历史上绝大多数人类的情况，并且仍然是发展中国家许多地区的情况。例如，大约27亿人（约占世界人口的40％）现在依靠传统的生物质燃料进行烹饪。这种低质量燃料可能是室内空气污染的主要来源。即使随着能源可获得性和经济发展的扩大，室内空气污染每年的死亡人数仍将超过150万人，这个数字高于疟疾和结核病的死亡率。

<br>随着全球化不断将世界各地的贸易网络联系在一起，各国可以通过进口增加和多样化其能源储备。然而，如果一个国家的发展水平低，而能源成本——这些成本越来越由全球金融力量决定——高昂，那么人们将缺乏能源，无论该国的能源储备有多大或多样化。因此，负担得起的一个重要条件是提高收入水平（因此提高购买力）并控制在全球层面运作的无人情的经济力量对人们日常面临的成本产生的影响。
<br>然而，如果能源供应不可靠，那么“可负担性”就毫无意义了。在许多发展中国家，能源资源经常很少，供应不稳定。如今，全球20%的人口仍然没有电力供应，更多人口则遭受持续的停电。2012年，印度发生了一次规模庞大的全国停电，影响了近7亿人，瘫痪了交通和通讯系统，并导致了不知道多少的死亡。这场灾难不仅由于供应问题，还由于管理不善和不发达的能源基础设施。因此，基本的经济活动取决于稳定的供应、强大的治理、高效稳定的分配系统。能源的可靠性有多个社会经济维度。

<br>电力、自动化交通和信息技术对经济发展至关重要。它们也是现代社会的基本特征，因此能够可靠和负担得起地满足这些需求的能源来源和系统可以被视为“现代化”。印度、撒哈拉以南非洲和其他发展中国家的人口增长将继续。人均经济消费也将增加，从而对上述服务产生更大的需求，并因此需要接入现代能源。在未来25年，大约90%的能源需求增长将来自非经济合作与发展组织（OECD）成员国，即富裕的西方经济体和日本之外的国家。满足这种不断增长的能源需求将是21世纪最重要的挑战之一，这也是它在可持续发展目标中占据如此重要地位的原因。这也带我们到SDG 7的最后一个维度：可持续性。

<br>能源应该产生稳定的电力，以满足基本的人类需求，维持和提高社会功能和生活水平。它还应尽可能地可持续发展，也就是说，能源使用所产生的能量应远大于所产生的废物和污染物。所有可持续能源都必须是现代的，尽管并非所有现代能源都可持续。煤炭或许是最重要的例子。在历史上，煤炭对于工业化和人类福祉的进步是不可或缺的。如果今天世界上更多的人们享有了以前无法想象的生活水平，很大程度上是因为煤炭。然而，除了丰富、广泛分布和易于使用等优点外，还有一长串严重的问题需要弥补，尤其是在人口增长和环境恶化的时代，这个问题仍在不断增长。
<br>今天，煤仍然提供了全球约40％的电力和几乎相同比例的全球碳排放量。煤也是效率低下的能源，其质量-能量比低，产生了巨大的污染。因此，煤在全球范围内既不可持续，因为它对人为气候变化的贡献，也不可持续在当地，因为它是对公共卫生和生态条件的威胁（除了燃烧的污染副产品外，煤矿开采过程也会带来无数的环境问题）。鉴于煤的使用规模和全球经济主要由化石燃料驱动的出现，我们应该怎么做？

<br>这些是需要实用、多方面的方法应对的挑战。解决方案需要在全球范围内寻找，政府和机构必须共同努力。国际气候变化协议是这些努力的最显著成果。可持续发展目标也有助于制定合作的基调，并促成了对优先事项的共识。在政策方面，向发展中国家转移清洁能源技术是一个重要的例子。事实上，国际气候变化协议——如清洁发展机制（CDM）——明确规定了此类转移。然而，这还不够。解决方案也必须在本地进行开发。有证据表明，尽管CDM的收益通常是必要的和净积极的，但并不总是能够到达本地层面，特别是在贫困的农村地区。发展应该对本地情况保持敏感，并识别能源政策的意外后果。在全球和区域层面上盲目追求生物燃料可能会导致意想不到但严重的环境退化。为生产棕榈油而毁林开荒破坏了当地的福祉，提醒我们面对的能源问题的复杂性。

<br>在21世纪的全球发展中，获得负担得起、可靠、可持续和现代化的能源是不可或缺的。现在还没有所有满足这一挑战所需的解决方案，而且已经存在的解决方案可能也不明显。如果国际组织具有足够的远见，如果政府能够共同合作，如果社区和个人得到正确的激励和必要的手段，那么找到这些解决方案并将它们与不同规模之间的目标协调一致是可行的。SDG 7至少是朝着这个方向迈出的重要一步。 

<br>包容、安全、具有弹性和可持续发展
<br>第11个目标是通过使城市和人类定居点包容、安全、有弹性和可持续来促进城市地区的可持续发展。目前许多人离开农村地区到城市地区寻找更好的机会，增加了城市地区的人口，尽管这种增长可能会导致各种问题，包括财务、社会和环境不平等。

<br>一个可持续发展的城市通过其活动减少环境影响，并根据其自身的领土、地理、社会、经济和文化条件促进可持续的消费和生产模式。它是一个对气候变化的影响具有抗性，减少其人口的脆弱性的城市。完美的可持续城市将是一个能够自给自足的能源城市，能够利用废弃物产生能源，具备更可持续的交通方式，维护绿色空间，并正确地管理和利用其自然资源。

<br>一个可持续的城市需要进行许多生态友好型规划，包括全市范围内的公共交通、行人和自行车友好型人行道、可持续的建筑以及使用可再生能源等。一个可持续城市最大的标志之一是它们切换到清洁能源的努力。因此，使用太阳能板是必要的，因为它将：

<br>财务上有益 - 降低电费账单
环保 - 每产生一千瓦时的太阳能电能显著减少二氧化碳等温室气体的排放，同时也减少了二氧化硫、氮氧化物和颗粒物等危险污染物的排放。太阳能还减少了水的消耗和提取。

<br>采取紧急行动应对气候变化及其影响。
气候变化指长期气温和天气模式的变化。这些变化可能是自然的，比如由于太阳循环的变化。但自19世纪以来，人类活动一直是气候变化的主要驱动力，主要是由于燃烧煤炭、石油和天然气等化石燃料。

<br>燃烧化石燃料会产生温室气体排放，它们像裹在地球周围的毯子一样，捕捉太阳的热量并提高温度。

<br>引起气候变化的温室气体排放的例子包括二氧化碳和甲烷。例如，驾驶汽车使用汽油或用煤炭供暖等都会产生这些气体。清理土地和森林也会释放二氧化碳。垃圾填埋场是甲烷排放的主要来源。能源、工业、交通、建筑、农业和土地使用是主要的排放源。
<br>人们以各种方式经历着气候变化。
<br>气候变化会影响我们的健康、种植粮食的能力、住房、安全和工作。我们中的一些人已经更容易受到气候影响的影响，例如生活在小岛国家和其他发展中国家的人们。像海平面上升和盐水侵入这样的条件已经发展到整个社区必须搬迁的地步，而持久性干旱正将人们置于饥荒的风险之中。预计在未来，“气候难民”的数量将增加。
<br>我们面临着巨大的挑战，但已经知道了许多解决方案。
<br>将能源系统从化石燃料转换为太阳能或风能等可再生能源将减少导致气候变化的排放。
<br>作为一种可再生的能源，太阳能在减少温室气体排放和缓解气候变化方面扮演着重要角色，这对保护人类、野生动物和生态系统至关重要。太阳能还可以改善空气质量，并减少能源生产的用水量。



<br>因此，如今使用太阳能电池板以减轻气候变化造成的影响是必要的。