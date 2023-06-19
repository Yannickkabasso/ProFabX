<!-- project/presentation.md -->
# SOLAR PANEL TRACKING ENERGY

<br>
Our final goal is to build a self solar tracking energy and the vision is to capture as much as possible sunlight as a source of radiant energy, which is converted into electric energy in the form of direct current electricity. The project is based on LDR sensor, we made the rotatable Solar system which has the home position during night time but when the light is available in day time the solar system automatically waking up through sensing the light presence and all the solar panels rotate counter clockwise and open like a sunflower and follow the sun rotation, after the sun fallen down all the solar panels are automatically rotate clockwise and go to the home position for next day sun light.
<br>
<br>
Our Solar Panel tracking energy is a technology for orienting a solar collector, reflector, or photovoltaic panel towards the sun. As the sun moves across the sky, a tracking device makes sure that the solar collector automatically follows and maintains the optimum angle to receive the most of the solar radiation

<h1 style="font-size:1.5vw"><span style="color:black">I. Required Materials</span></h1>

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
                            <h3 class="title">Solar Panels(6pcs,6v each)</h3>
                        </div>
                    </div>
                </div>

<div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/battery.jpg">
                        <div class="team-content">
                            <h3 class="title">12V Li ion Battery</h3>
                        </div>
                    </div>
                </div>

<div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/nano.jpg">
                        <div class="team-content">
                            <h3 class="title">Arduino nano v3</h3>
                        </div>
                    </div>
                </div>
                 <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/l293d.jpg">
                        <div class="team-content">
                            <h3 class="title">L293d ic driver + ic base</h3>
                         </div>
                     </div>
                 </div>

<div class="row">
                     <div class="col-md-4 col-sm-6">
                         <div class="our-team">
                                 <img src="images/regulator.jpg">
                             <div class="team-content">
                                 <h3 class="title">7806 regulator</h3>
                        </div>
                    </div>
                </div>


<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/resistor.jpg">
                        <div class="team-content">
                            <h3 class="title">10k carbon film resistor</h3>
                        </div>
                    </div>
                </div>
                <div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/ldr.jpg">
                        <div class="team-content">
                            <h3 class="title">ldrs</h3>
                        </div>
                    </div>
                </div>
                <div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/servo.jpg">
                        <div class="team-content">
                            <h3 class="title">servo motor</h3>
                        </div>
                    </div>
                </div>
<div class="row">
                 <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/gear.jpg">
                        <div class="team-content">
                            <h3 class="title">n20 gear motor</h3>
                         </div>
                     </div>
                 </div>
                <div class="row">
                     <div class="col-md-4 col-sm-6">
                         <div class="our-team">
                                 <img src="images/header.jpg">
                             <div class="team-content">
                                 <h3 class="title">male & female headers</h3>
                        </div>
                    </div>
                </div>

<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/pcb.jpg">
                        <div class="team-content">
                            <h3 class="title">printed circuit board (pcb)</h3>
                        </div>
                    </div>
                </div>

<div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                            <img src="images/switch.jpg">
                        <div class="team-content">
                            <h3 class="title">limit switches</h3>
                        </div>
                    </div>
                </div>
</div>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">II. Software Used</span></h1>

<a href="https://www.arduino.cc/en/software" class="fab fa-facebook"><span style="font-size:1.2vw">Arduino IDE</span></a>
<br>
<br><a href="https://easyeda.com/" class="fab fa-facebook"><span style="font-size:1.2vw">EasyEDA</span></a>
<br><br><a href="https://www.autodesk.com/products/fusion-360/free-trial" class="fab fa-facebook"><span style="font-size:1.2vw">Fusion 360</span></a>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">III. Fusion 360 parts</span></h1>

<br>

<img src="images/fusion.jpg" alt="fusion.jpg" max-width="1200" height="800">

<br>
<h1 style="font-size:1.5vw"><span style="color:black">IV. How to make </span></h1>

<br>
We first bought the materials and printed the 3D parts 
<br>

<img src="images/allparts.jpg" alt="allparts.jpg" max-width="1200" height="800">

<br>After we used Easyeda to design the schematic and made our self custom pcb
<br><div class="loader"><img src="images/pcb.png" alt="#" /></div>
<br><div class="loader"><img src="images/pcb1.jpg" alt="#" /></div>

<br><br>
Now before we can try out the self custom pcb, we compiled and upload the codes to the arduino nano. The codes for this project can be found here.

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

After, we created a gerber file and orderd a custom pcb from [NEXTPCB](https://passport.hqonline.com/register?reurl=https%3A%2F%2Fwww.nextpcb.com%2Fregister%3Fcode%3Dtechboysxwd)

<br><div class="loader"><img src="images/nextpcb.jpg" alt="#" /></div>
<br><div class="loader"><img src="images/pcbf.jpg" alt="#" /></div>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">Solar Panels connection </span></h1>
<br><div class="loader"><img src="images/solar panel.jpg" alt="#" /></div>
<br> 
<br> We are going to use 6 pieces of solar panel and each has 6V 70mAh power output, We will wire the one pair of panels in series and 3 pairs in parallel, then the voltage output will be 6+6=12v, So basically when the panels are fully opened the voltage output is 12V and when the panel goes on in home position the voltage output will be 1-3 volts.
<br><div class="loader"><img src="images/solars.jpg" alt="#" /></div>
<br><div class="loader"><img src="images/solarm.jpg" alt="#" /></div>
<br><div class="loader"><img src="images/solaro.jpg" alt="#" /></div>
<br>
<br> 
<h1 style="font-size:1.2vw"><span style="color:black">LDRS and Working Principle </span></h1>
<br>Light depending resistor is a photo-resistor, which decrease the resistance when the light increases.
An LDR or photo-resistor is made any semiconductor material with a high resistance. It has a high resistance because there are very few electrons that are free and able to move – the vast majority of the electrons are locked into the crystal lattice and unable to move. Therefore in this state there is a high LDR resistance.
<br>As light falls on the semiconductor, the light photons are absorbed by the semiconductor lattice and some of their energy is transferred to the electrons. This gives some of them sufficient energy to break free from the crystal lattice so that they can then conduct electricity. This results in a lowering of the resistance of the semiconductor and hence the overall LDR resistance.The process is progressive, and as more light shines on the LDR semiconductor, so more electrons are released to conduct electricity and the resistance falls further.
<br><div class="loader"><img src="images/solarl.jpg" alt="#" /></div>
<br>You can see the fifth resistor is placed on the middle position of the solar top,
when the light is minimum, the micro controller Arduino read the resistance value and the the threshold value is sated in the coding section, when the light is available and the threshold level breaks, the Arduino rotate the n20 gear motor anticlockwise through the L293D Driver till the limit switch level high, when anticlockwise limit switch pressed the panel stop rotating and panel is fully opened position when the button is pressed, now the main work is going to progress, according the sun rotation other 4 LDRs sense the light and send data to the Arduino, and Arduino process the data then rotate the servo motors according the sun rotation, the rotation position of the servo is max 170 degrees,when the sun goes down the fifth LDR sense data again and this time the process is reverse condition, the LDR data goes down blow the threshold level and Arduino Rotate the N20 motor clockwise till the 2nd limit switch press and run the servo in home position, when light is available in next day the same process goes on again.
<br>
<h1 style="font-size:1.5vw"><span style="color:black">Project Circuit</span></h1>  
<br><div class="loader"><img src="images/solara.jpg" alt="#" /></div>

<br>
<h1 style="font-size:1.5vw"><span style="color:black">Trials</span></h1>  
<br><br>
<img src="images/trial1.gif" alt="trial1.gif" max-width="1000" height="700">
<br><br>
<img src="images/trial2.gif" alt="trial2.gif" max-width="1000" height="700">
<br><br>
<img src="images/trial3.gif" alt="trial3.gif" max-width="1000" height="700">
<br>
<br>
<br><h1 style="font-size:1.5vw"><span style="color:black">Final design with Power and current display (voltage=11.14v, current=445mA and the power=4.978W)</span></h1> 
<br><div class="loader"><img src="images/display.jpg" alt="#" /></div>
<br><br><div class="loader"><img src="images/displayp.jpg" alt="#" /></div>
<br><br><div class="loader"><img src="images/displaypo.jpg" alt="#" /></div>
<br>
<h1 style="font-size:1.5vw"><span style="color:black">Demo</span></h1> 
<br><br>
<img src="images/demo.gif" alt="demo.gif" max-width="1000" height="700">

<br>
<h1 style="font-size:1.5vw"><span style="color:black">Innovation</span></h1>
Our Solar Panel Tracking Energy have 6 panels rotating at a 90-degree angle, producing 40% more energy than fixed solar panels. They work with a dual-axis tracking system, so they always face the sun — increasing productivity by up to 10%. Their elevated design also allows the panels to cool naturally, increasing their efficiency.

<br>
<br>
<h1 style="font-size:1.5vw"><span style="color:black">Solar Flower Market- Global Industry Analysis and Forecast (2022-2029)</span></h1>
<br>The Global Solar Flower Market was valued at US $14 million in 2022 and is predicted to reach 39.20 million in 2028, at a compound annual growth rate of ( CAGR )16.00% between 2023 and 2028.

<br>Main benefits: Solar flower is a ground-mounted, all-in-one solar system with a tracker that follows the sun. It utilizes advanced automation to quickly monitor the sun, manufacturing up to 40% additional power than conventional static solar panels.
<br>Along with this, the solar flower possesses a unique feature of self-cleansing. Increase in recognition about the utilization of solar power and increase in advantages towards encouragement of sustainable power are major elements operating the global solar flower market. 
<br>Cons:However, the high initial investment and lack of skill professionals are the major factors restraining the global solar flower market.
<br>
<h1 style="font-size:1vw"><span style="color:black">Top Impacting Factors</span></h1>
Execution of strict rules to assist environmental preservation increases the energy industry to move to clean environment-friendly power resources. Moreover, the prices of power created using solar power is expected to decrease in the coming years, due to technological advancements.

<br>
<h1 style="font-size:1vw"><span style="color:black">Market Trends</span></h1>
● Awareness towards Environment and Use of Renewable Resources for Energy Generation Process
<br>● With increase in awareness about the carbon emission from several non-renewable resources and the rise in prices of fuels, the solar flower market is expected to have a surge in demand.
<br>● Favorable Government Policies and Priority is Key Driver for Market Growth
<br>● Technological Advancements and Increase in R&D Programs in Solar Energy Field is a Positive Factor for Growth of Market
<br>● Increase in demand for eco-friendly sources of energy coupled with advancement in the field of solar power generation technique had a positive impact on the market of solar flower.

<br>
<h1 style="font-size:1vw"><span style="color:black">Solar Flower Market Segment Analysis:</span></h1>

<br>Solar Flower Market is divided by: 
<br>Connectivity (On Grid and Off Grid)
<br>The off-grid segment is expected to enlarge at a quicker CAGR throughout the projected period.
<br>Application (Residential area, Schools and Universities, Recreational Parks, Mountainous Region, and Others)
<br>The schools and universities segment are estimated to enlarge at a quicker rate, due to the enormous scale implementations of solar flowers located in Europe and the U.S. 
<br>Region (North America, Europe, Asia Pacific, Middle East and Africa, and Latin America)
<br>North America is estimated to be the dominant region in the solar flower market. Development in expenditure in solar implementations is the major factor estimated to increase the market in the zone in the coming year. The U.S influenced the solar flower market in North America in 2021. 
<br>In July 2021, Virginia Wesleyan University became one of the first institutes in the nation to implement the smart flower, an advanced kind of solar function. The Asia Pacific is an alternate major zone of the worldwide solar flower market.


<h1 style="font-size:1.5vw"><span style="color:black">Key Tech Analysis</span></h1>
<h1 style="font-size:1vw"><span style="color:black">*01 Photovoltaic Cell (Solar PV) </span></h1>
<br><div class="loader"><img src="images/solar-photovoltaic-pv.jpeg" alt="#" /></div>
<br>Solar PV generation increased by a record 179 TWh (up 22%) in 2021 to exceed 1 000 TWh. It demonstrated the second largest absolute generation growth of all renewable technologies in 2021, after wind. Solar PV is becoming the lowest-cost option for new electricity generation in most of the world, which is expected to propel investment in the coming years. However, average annual generation growth of 25% in the period 2022-2030 is needed to follow the Net Zero Emissions by 2050 Scenario. This corresponds to a more than threefold increase in annual capacity deployment until 2030, requiring much greater policy ambition and more effort from both public and private stakeholders, especially in the areas of grid integration and the mitigation of policy, regulation and financing challenges. This is particularly the case in emerging and developing countries.

<br>
<h1 style="font-size:1vw"><span style="color:black">*02 Arduino Nano v3</span></h1>
<br><div class="loader"><img src="images/v3.webp" alt="#" /></div>
<br>The Arduino Nano is a small, complete, and breadboard-friendly board based on the ATmega328 (Arduino Nano 3.x). It has more or less the same functionality of the Arduino Duemilanove, but in a different package. It lacks only a DC power jack, and works with a Mini-B USB cable instead of a standard one. The Arduino Nano can be powered via the Mini-B USB connection, 6-20V unregulated external power supply (pin 30), or 5V regulated external power supply (pin 27). The power source is automatically selected to the highest voltage source.
<br>Each of the 14 digital pins on the Nano can be used as an input or output, using pinMode(), digitalWrite(), and digitalRead() functions. They operate at 5 volts. Each pin can provide or receive a maximum of 40 mA and has an internal pull-up resistor (disconnected by default) of 20-50 kOhms. In addition, some pins have specialized functions:
<br>

* Serial: 0 (RX) and 1 (TX). Used to receive (RX) and transmit (TX) TTL serial data. These pins are connected to the corresponding pins of the FTDI USB-to-TTL Serial chip.
* External Interrupts: 2 and 3. These pins can be configured to trigger an interrupt on a low value, a rising or falling edge, or a change in value. See the attachInterrupt() function for details.
* PWM: 3, 5, 6, 9, 10, and 11. Provide 8-bit PWM output with the analogWrite() function.
* SPI: 10 (SS), 11 (MOSI), 12 (MISO), 13 (SCK). These pins support SPI communication, which, although provided by the underlying hardware, is not currently included in the Arduino language.
* LED: 13. There is a built-in LED connected to digital pin 13. When the pin is HIGH value, the LED is on, when the pin is LOW, it's off.
<br>The Nano has 8 analog inputs, each of which provide 10 bits of resolution (i.e. 1024 different values). By default they measure from ground to 5 volts, though is it possible to change the upper end of their range using the analogReference() function. Analog pins 6 and 7 cannot be used as digital pins. Additionally, some pins have specialized functionality:
<br>
* I2C: A4 (SDA) and A5 (SCL). Support I2C (TWI) communication using the Wire library (documentation on the Wiring website).
<br>
There are a couple of other pins on the board:

* AREF. Reference voltage for the analog inputs. Used with analogReference().
* Reset. Bring this line LOW to reset the microcontroller. Typically used to add a reset button to shields which block the one on the board.

<h1 style="font-size:1vw"><span style="color:black">*03 L293D IC Driver</span></h1>
<br><div class="loader"><img src="images/L293D.webp" alt="#" /></div>
<br>The L293D is a dual-channel H-Bridge motor driver capable of driving a pair of DC motors or a single stepper motor. This means it can drive up to two motors individually it's also one of the cheapest and easiest way to control dc motors through arduino boards, which makes it ideal for building this project.

<br>The L293D is most often used to drive motors, but can also be used to drive any inductive load such as a relay solenoid or large switching power transistor.It is capable of driving four solenoids, four uni-directional DC motors, two bi-directional DC motors or one stepper motor.

<br>
<h1 style="font-size:1vw"><span style="color:black">*04 PCB</span></h1>
<br><div class="loader"><img src="images/npcb.jpg" alt="#" /></div>
<br>One of the key concepts in electrical and electronics is the printed circuit board(PCB). It allows component to connect to one another in a safe and controlled manner. It is a board that has lines and pads that connect various points together, it also allows signals and power to be routed between physical devices
<br>Electrical components may be fixed to conductive pads on the outer layers in the shape designed to accept the component's terminals, generally by means of soldering, to both electrically connect and mechanically fasten them to it.

<br>
<h1 style="font-size:1.5vw"><span style="color:black">Our Project and the UN Sustainable Delevelopment Goals (SDGs)</span></h1>
<br>
The UN adopted 17 Sustainable Development Goals to improve People's leaving condition in the world.
<br>The Sustainable Development Goals are a call for action by all countries – poor, rich and middle-income – to promote prosperity and a better quality life while protecting the planet. They recognize that ending poverty and other deprivations must go hand-in-hand with strategies that build economic growth and address a range of social needs including social protection, health, education, job opportunities and reduce inequality, while tackling climate change and environmental protection.



<br>Our Project (Solar Pannel, power supply system) is in accordance with some of the UN SDGs Goals. As we all know, electricity is an indispensable part of daily life, and the generation of electricity marks the further liberation of productivity. Power system refers to completing the generation, transformation, transmission and distribution of electric energy. With the rapid change of science and technology, power technology has made great progress, and humans have also entered the electrical information area. Only a reliable, safe and affordable power supply and distribution system can ensure the normal work and life environment. Information technology and other high and new technology are built on the basis of electricity application, electric energy occupies a very important position in modern industrial production and the society at large.

<br>Our project include three of the SDGs Goals:

* SDG Goal 7 Affordable and Clean Energy
* SDG Goal 11 Sustainable Cities and Communities
* SDG Goal 13 Climate Action

<br>The sustainable development goals (SDGs) proposed by the Open Working Group of the General Assembly of the United Nations recognize the importance of the natural environment and its resources to human well-being. As a whole, it is definitely a worthy charter for the twenty-first century, as it addresses the diverse challenges that we face as a global community. SDG 7—to “ensure access to affordable, reliable, sustainable and modern energy for all”—is a challenge confronting every country, that touches everyone. To understand the necessity of meeting this goal, and what is required to do so, we should unpack the statement of the goal itself. The four dimensions of SDG 7 are affordability, reliability, sustainability and modernity. These different dimensions are not mutually exclusive. They overlap, and in some cases even entail each other.

<br>Consider what it means to have access to affordable energy. The heterogeneity of energy use across the world is due largely to different natural resource endowments and purchasing power. For example, a country with large coal deposits will likely make wide use of this resource to industrialize its economy. The people living within this country will likely use it as the primary means of power generation.
<br>On the other hand, people living in places without ready stocks of fossil fuels may rely on more primitive methods of combustion, such as wood fibers or perhaps even animal dungs. Indeed, this is the condition that prevailed for the vast majority of humankind throughout its history, and continues to be the condition for many parts of the developing world. For instance, approximately 2.7 billion people (about 40 per cent of the world’s population) now rely on traditional biomass fuels for cooking. Such low-quality fuels can be a major source of indoor air pollution. Even with the expansion of energy accessibility and economic development, the annual death toll from indoor air pollution will still be over 1.5 million people—a higher rate than that from both malaria and tuberculosis.

<br>As globalization continues to bind the world in deeper networks of trade, countries can augment and diversify their energy endowments by import. However, if the development level of a country is low and the costs of energy—which are increasingly determined by global financial forces—are high, then people will lack access to energy no matter how large or diverse its country’s endowment. Thus, an essential condition of affordability is raising income levels (and hence purchasing power) and controlling the impacts that impersonal economic forces operating at global levels have on the costs that people face on an everyday basis.

<br>Affordability is meaningless, however, if energy provision is unreliable. In many parts of the developing world, energy sources are often scarce and their supply intermittent. Today, 20 per cent of the world’s population still lacks access to electricity, and a larger share suffers from persistent power failures.3 In 2012, the massive, nationwide blackout that struck India affected nearly 700 million people, paralyzing transportation and communication systems and causing an unknown number of fatalities. This disaster was caused not just by supply issues, but also by mismanagement and an underdeveloped energy infrastructure. Thus, basic economic activity depends on a steady supply, robust governance, and an efficient and stable distribution system. There are multiple socioeconomic dimensions of energy reliability.

<br>Electricity, automated transportation and information technology are essential to economic development. They are also basic features of modern society, and thus energy sources and systems that meet these needs reliably and affordably can be considered as “modern”. Population growth will continue in India, sub-Saharan Africa, and other parts of the developing world. Per capita economic consumption will also increase, creating much greater demand for the services described above, and consequently for access to modern energy. Over the next quarter century, about 90 per cent of the growth in energy demand will come from countries that are not members of the Organization for Economic Co-operation and Development (OECD), i.e., countries outside of the rich Western economies and Japan.5Meeting this rising wave of energy demand will be one of the paramount challenges of the twenty-first century, and is a reason why it occupies such a central place in the SDGs. It also brings us to the final dimension of SDG 7: sustainability.

<br>Energy should generate a consistent stream of power to meet basic human needs, maintain and improve social functioning, and advance living standards. It should also fulfill these functions as sustainably as possible—that is to say, the power generated by energy use should be much greater than the resulting waste and pollution. All sustainable energy must be modern, although not all forms of modern energy are sustainable. Coal is perhaps the most important case in point. Historically, coal has been indispensable to industrialization and the advancement of human well-being. If more of the world’s people enjoy previously unimaginable living standards today, it is in large part because of coal. Offsetting its many virtues—for instance, abundance, wide distribution, and ease of use—is a long list of serious problems, however. In an age of population growth and environmental decline, this list is still growing.

<br>Today, coal still provides about 40 per cent of the world’s electricity and nearly the same fraction of global carbon emissions. Coal is also inefficient, with a low mass-to-energy ratio, and creates enormous pollution. Thus, coal is neither sustainable at the global scale because of its contribution to anthropogenic climate change, nor at the local scale because it is a threat to public health and ecological conditions (in addition to the polluting by-products of combustion, the process of coal mining creates myriad environmental problems). Given the scale of the use of coal, and the emergence of a global economy powered largely by fossil fuels, what can be done?

<br>These are challenges that require a pragmatic, multi-faceted approach. Solutions need to be found at the global scale, where Governments and agencies must work together. International climate change agreements are the most visible fruits of such efforts. The SDGs have also helped set the tenor for cooperation and contributed to an emerging consensus on priorities. In terms of policies, the transfer of clean energy technologies to developing countries is an important example. Indeed, international climate change agreements—such as the clean development mechanism (CDM)—explicitly provide for such transfers. This is not enough, however. Solutions must also be developed locally. There is evidence that benefits from CDM, while necessary and net-positive generally, do not always reach the local level, particularly in impoverished rural areas. Development should be sensitive to local conditions, and identify unintended consequences of energy policies. The heedless pursuit of biofuels at the global and regional levels may result in unintended yet severe environmental degradation. The countless acres of land deforested for palm oil undermine local well-being, and provide a stark reminder of the complexity of the energy problems that we face.

<br>Access to affordable, reliable, sustainable and modern energy is integral to global development in the twenty-first century. Not all the solutions needed to meet this challenge are yet available, and those that are may not be apparent. Figuring out these solutions and aligning them across scales will be difficult. Yet the task is achievable if international organizations have sufficient vision, if Governments can work together, and if communities and individuals are offered the right incentives and the necessary means. SDG 7 is, at the very least, an important step in that direction.   

<br>INCLUSIVE, SAFE, RESILIENT AND SUSTAINABLE
<br>The 11th goal is to promote sustainable development on urban areas by making cities and human settlements inclusive, safe, resilient, and sustainable.
Currently many people leave the rural areas to find better opportunities in the urban areas increasing the population in the urban areas, although this growth can lead to a variety of problems, including financial, social and environmental inequalities 

<br>A sustainable city reduces environmental impacts through its activities and promotes sustainable consumption and production patterns in accordance with its own territorial, geographical, social, economic, and cultural conditions. It is a city that is resilient to the impacts of climate change reducing the vulnerabilities of its population. The perfect sustainable city would be one that is self-sufficient in energy, manages waste to produce energy, has more sustainable transport, maintains green spaces and manages and uses its natural resources correctly.

<br>A sustainable city requires a lot of eco-friendly planning including CITY-WIDE ACCESS TO PUBLIC TRANSPORTATION; PEDESTRIAN- AND BIKE-FRIENDLY SIDEWALKS; SUSTAINABLE ARCHITECTURE the use of renewable energy and so on. One of the biggest indicators of a sustainable city is their efforts to switch to clean energy. Consequently, the use of solar panels is necessary as it will be:

<br>Financially beneficial- lower electricity bill
Environmentally friendly- Each kilowatt-hour (kWh) of solar that is generated will substantially reduce greenhouse gas emissions like CO2, as well as other dangerous pollutants such as sulfur oxides, nitrogen oxides and particulate matter.  Solar also reduces water consumption and withdrawal.


<br>Take urgent action to combat climate change and its impacts.
Climate change refers to long-term shifts in temperatures and weather patterns. These shifts may be natural, such as through variations in the solar cycle. But since the 1800s, human activities have been the main driver of climate change, primarily due to burning fossil fuels like coal, oil and gas.

<br>Burning fossil fuels generates greenhouse gas emissions that act like a blanket wrapped around the Earth, trapping the sun’s heat and raising temperatures.

<br>Examples of greenhouse gas emissions that are causing climate change include carbon dioxide and methane. These come from using gasoline for driving a car or coal for heating a building, for example. Clearing land and forests can also release carbon dioxide. Landfills for garbage are a major source of methane emissions. Energy, industry, transport, buildings, agriculture and land use are among the main emitters.
<br>People are experiencing climate change in diverse ways.
<br>Climate change can affect our health, ability to grow food, housing, safety and work. Some of us are already more vulnerable to climate impacts, such as people living in small island nations and other developing countries. Conditions like sea-level rise and saltwater intrusion have advanced to the point where whole communities have had to relocate, and protracted droughts are putting people at risk of famine. In the future, the number of “climate refugees” is expected to rise.
<br>We face a huge challenge but already know many solutions.
<br>Switching energy systems from fossil fuels to renewables like solar or wind will reduce the emissions driving climate change.
<br>As a renewable source of power, solar energy has an important role in reducing greenhouse gas emissions and mitigating climate change, which is critical to protecting humans, wildlife, and ecosystems. Solar energy can also improve air quality and reduce water use from energy production.



<br>So the use of solar panel is necessary nowadays to mitigate the impacts caused by climate change.