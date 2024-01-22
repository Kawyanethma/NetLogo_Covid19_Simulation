# NetLogo Covid-19 Model
## What is Netlogo?
NetLogo is a multi-agent programmable modeling environment that is used by many hundreds of thousands of students, teachers, and researchers worldwide. It is designed to be “low threshold and no ceiling” [^1] and teaches programming concepts using agents in the form of turtles, patches, links, and the observer. NetLogo allows exploration by modifying switches, sliders, choosers, inputs, and other interface elements. It comes with an extensive model’s library including models in a variety of domains such as economics, biology, physics, chemistry, psychology, and system dynamics. 

## About this Model
Inspired in the covid-19 (aka coronavirus), this simplified model simulates the transmission of a virus in a human population. The model can be initialized with 0-500 people. This model basic components and functionalities are,

* ***Population*** – With the population slider total population can be change 0 – 500 range.

* ***Degree of immunity*** – there is two parameters you can change to change immunity; you can change number of masks wearing population and there is switch to set vaccination status. 

* ***Duration of infectiousness*** - How long is a person infected before they either recover or die? This length of time is essentially the virus's window of opportunity for transmission to new hosts. In this model, duration of infectiousness is determined by the `%infectiousness`

* ***Hard-coded parameters*** - Four important parameters of this model are set as constants in the code. duration of immunity is set to 100 days. And when vaccinated it increased to 500.

> [!IMPORTANT]
> ***death of turtle***: sick-time > 50  <br>
> ***Recovery of turtle*** : after 500 days

 ## Netlogo UI Design
The WORLD displays the core of the simulation which lies in the activities of the turtles represented by the PERSON shape.

### Colors of turtles 
To identify each agent I used colors, those are, 
* Red:  if person is infected color is red
* Blue:  if person is wearing a mask color is blue
* Green: if person is uninfected color is green.
* Grey: If person is died color is grey.
* Orange: if person is recovered color, is orange. 



## _References_

[^1]: https://ccl.northwestern.edu/2005/BlikAbrWil_IDC-05-demo.doc.pdf.
[^2]: https://www.netlogoweb.org/launch#http://ccl.northwestern.edu/netlogo/community/CoronaVirus.nlogo.
[^3]: https://www.netlogoweb.org/launch#http://ccl.northwestern.edu/netlogo/community/COVID-19%20Transmission%20Model.nlogo.
