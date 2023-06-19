<!-- project/intro.md -->
# INTELLIGENT DUSTBIN
<br>

### I. Background Info

Good waste management has become an essential issue for our planet. In public and natural spaces, many do not pay attention to the waste they leave behind. When there is no garbage collector available, it is easier to leave waste on site than bring them back. Even the so called preserved spaces are polluted by waste. So our AI based is designed for homes, offices, streets and public places. It simplifies recycling, sorts and compresses the waste automatically, It controls the fill level and processes data for convenient waste management.
<br><div class="loader"><img src="images/garbage1.jpg" alt="#" /></div>

<br>To preserve natural areas, homes and offices it is important to provide well-managed waste collection points :
<br><br>
<br>To prevent them from overflowing, the bins must be raised regularly. It is hard to get through the right time : too soon, and the trash can be empty, too late and the trash can overflow. This problem is all the more critical when the bin is difficult to access (such as on hiking trails in the mountains)

<br><br><div class="loader"><img src="images/garbage2.jpg" alt="#" /></div>
<br><br>
In this rational waste management, sorting can be a major challenge. Organics waste can be directly processed by nature, in composting. Non organics waste must be collected to be treated by specific processes.

<br><br>

<h1 style="font-size:1.5vw"><span style="color:black">Purpose of the Project</span></h1>

The purpose of our project is to provide a supervision device for intelligent waste bin. This device integrates several sensors to supervise the state of the trash.

- Level sensor: based on ultrasonic system, used to prevent overflows by alerting the garbage collection team.

- Temperature and humidity sensor: used to monitor the trash environment. This can be useful to manage the condition of organic compost, and to prevent contamination in some specific case (very wet or hot conditions, risk of fire in very dry conditions)

- Flame sensor: some may deposit incandescent waste (like cigarette butts) or may intentionally set fire to the bin. A garbage fire can have dramatic effects on the environment (for example it can cause a forest fire). The flame sensor can alert supervision team about the problem.

- Moisture sensor : for the compost process, it is important to maintain a certain humidity level in the compost material. The moisture sensor, included in our project, will measure the humidity level on the compost.

- Opening sensor : a opening detector will be installed on the trash lid to get statistics on garbage use and detect bad closure.

- Voice sensor : a mic will be installed on the trash (for homes and offices )

- Location system : garbage must be identified and localized to help garbage collection team on their management. It will offer more agility on the garbage location management, with the possibility to deploy temporary garbage bins (eg. In summer on beach and hiking tracks, in winter on ski slope, on special events such as sports competition of music festivals)
<br>The project takes on its full meaning with a waste bin with two compartments:

- One for non organics waste.
- One for organic waste with composting process.
<br>
<br><br><br><br><div class="loader"><img src="images/garbage3.avif" alt="#" /></div>

<br>
<br><br>

<h1 style="font-size:1.5vw"><span style="color:black">Sigfox Usage</span>(Still looking for more convinient)</h1>

The trash will be install in isolated areas. The power will be provide by battery, possibly connected to a solar panel. For us, Sigfox seams to be a very good solution so far:

- Sigfox communication system has a wide area coverage : its allows to deploy the project on a large scale.

- Sigfox system provides sufficient communication capabilities for our use case.

- Sigfox can provide a 100m localization solution : not necessary to add a GPS shield on the bin.

- Sigfox is a low power solution, which allows the device to operate a long time autonomously.

<br><br>
<br>

### Project Details

Example of Hardware Design Method

<br><br><br><br><div class="loader"><img src="images/diagram.avif" alt="#" /></div>
<br><br>
<br><br>

<h1 style="font-size:1.5vw"><span style="color:black">Project Steps</span></h1>

<h1 style="font-size:1vw"><span style="color:black">Step 1: Understand Sigfox</span></h1>

Sigfox is a solution to connect the device in scope of Internet of Things. It’s currently operated in 45+ countries and 3 millions + devices. The message can be up to 12 bytes which maximum of 140 uplink and 4 downlink per day.

<h1 style="font-size:1vw"><span style="color:black">Step 2: Hardware Lookup</span></h1>

<br><br><br><br><div class="loader"><img src="images/harwares.avif" alt="#" /></div>

