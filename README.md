# House_Temperature_Control
The goal is to control the temperature in a house, having the indoor and outdoor temperature, and the heat generated in the house.

<h3> &nbsp;Design of the driver of a heater</h3>

I used an **LM358 IC** along with a **TIP41 transistor**, and a 10 volts **power supply** where by changing the input voltage from 0 to 8 voltes, the output power of the heater changes from 0 to 100 percent.

Transfer function of the heater driver:

$Gd(s) = \frac{Vout(s)}{Vin(s)}\$

<h3> &nbsp;The open-loop controller</h3>

The top level open-loop controller that should be implemented is as follows:

By using the transfer functions above, I implemented the open-loop controller as below in Simulink:

<img src="images/IMG_4984.jpg" width="700" height="270">


The outputs of the temperature of the house, and Gs are shown below:

Output of the house:

<img src="images/IMG_4987.jpg" width="400" height="350">


Output of Gs:

<img src="images/IMG_4986.jpg" width="400" height="350">

<h3> &nbsp;The closed-loop controller</h3>

I implemented a closed-loop PI controller as below, which will make the temperature of the house stable on 26 centigrades in less than 40 seconds: 

<img src="images/IMG_4993.jpg" width="700" height="270">

The output:

<img src="images/IMG_4995.jpg" width="400" height="350">

The implementation of the PI controller using operational amplifiers:

<img src="images/IMG_4997.jpg" width="700" height="270">

I tested the designed circuit for 3 different values of Tout: 2, 10, and 15.

The circuit implementation is as below:

<img src="images/IMG_4998.jpg" width="600" height="600">

Output corresponding to the temprature of the house:

<img src="images/IMG_4999.jpg" width="400" height="350">

Output of the controller:

<img src="images/IMG_5001.jpg" width="400" height="350">

Output corresponding to Gsc:

<img src="images/IMG_5002.jpg" width="400" height="350">

<h3> &nbsp;The on/off controller</h3>The on/off controller

Consider the open-loop system below, where a relay is used instead of the driver of the heater.

![My Image](images/1.png)

The closed-loop circuit above with the relay in Simulink:

<img src="images/IMG_5003.jpg" width="600" height="300">

Output corresponding to the temprature of the house:

<img src="images/IMG_5004.jpg" width="400" height="350">

Output of the controller(relay):

<img src="images/IMG_5005.jpg" width="400" height="350">

Output corresponding to Gsc, along with the input source:

<img src="images/IMG_5006.jpg" width="400" height="350">

Implementation of a controller which keeps the temperature of the house between 24 to 28 degrees.

The closed-loop circuit in Simulink:

<img src="images/IMG_5009.jpg" width="600" height="300">

Output corresponding to the temprature of the house:

<img src="images/IMG_5008.jpg" width="400" height="350">

Output of the controller(relay):

<img src="images/IMG_5018.jpg" width="400" height="350">

Output corresponding to Gsc, along with the input source:

<img src="images/IMG_5011.jpg" width="400" height="350">

Now testign the designed circuit for 3 different values of Tout: 2, 10, and 15.

The circuit implementation is as below:

<img src="images/IMG_5012.jpg" width="600" height="600">

Output corresponding to the temprature of the house:

<img src="images/IMG_5015.jpg" width="400" height="350">

Output of the controller:

<img src="images/IMG_5014.jpg" width="400" height="350">

Output corresponding to Gsc:

<img src="images/IMG_5013.jpg" width="400" height="350">

As we can see from the results, the outputs of the house and the controller are without change, and the changes in the out put of the sensor can be ignored since the controller is closed-loop. 
