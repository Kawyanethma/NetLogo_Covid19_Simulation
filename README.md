# NetLogo Covid-19 Model
## What is Netlogo?
NetLogo is a multi-agent programmable modeling environment that is used by many hundreds of thousands of students, teachers, and researchers worldwide. It is designed to be “low threshold and no ceiling” [^1] and teaches programming concepts using agents in the form of turtles, patches, links, and the observer. NetLogo allows exploration by modifying switches, sliders, choosers, inputs, and other interface elements. It comes with an extensive model’s library including models in a variety of domains such as economics, biology, physics, chemistry, psychology, and system dynamics. [^2][^3]

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
* ***Red***:  if person is infected color is red
* ***Blue***:  if person is wearing a mask color is blue
* ***Green***: if person is uninfected color is green.
* ***Grey***: If person is died color is grey.
* ***Orange***: if person is recovered color, is orange.

### Interface items
There are different interface items in this model,
* ***Setup button*** - Used to initialize the model’s state. It is used to set the initial values of variables, create agents and etc.
* ***Go button*** - Used to start the simulation of model.
* ***CovidPerson switch*** – This switch adds one covid infected person to world.
* ***Vaccination switch*** – This switch change vaccination status to true for all agent in the WORLD.
* ***Population Slider*** – You can change population of the world.
* ***Maskedup Slider*** – You can change number of people that wearing mask in the world.
* ***Days Monitor*** – It show the number of days.
* ***Recover Monitor*** – It displays percentage of recovered people.
* ***Infected Monitor*** – It displays percentage of infected people.
* ***Died Monitor*** – It displays percentage of died people.
* ***Population Status Plot*** – This plot shows Status of the people in this model. This plot has three plot pens, 

> [!NOTE]
> ***infected*** – this shows infected people percentage of world.
> `set %infected (count turtles with [color = red] / count turtles)* 100`

> [!NOTE]
> ***recover*** – this shows recover people percentage of world.
> `set %recover (count turtles with [color = orange] / count turtles)* 100`

> [!NOTE]
> ***died*** – this shows died people percentage of world. 
> `set %died (count turtles with [color = grey] / count turtles)* 100`

> [!NOTE]
> ***uninfected*** – this shows uninfected people percentage of world.
> `set %uninfected 100 - %infected`
### _UI of the model_
<img src="https://github.com/Kawyanethma/NetLogo_Covid19_Simulation/assets/92635894/e405dee5-a229-421a-9a65-7951b35c30b8" 
 alt="UI of the model"
 title="UI of the model"
 align="center"
 width="700"/>

 ## Thing to try 
 1.	***Change initial conditions***:
    * Change `population` slider to change the initial number of agents in this model.
    * Change `maskedup` slider to change number people wearing masks .
    * By turn on or off `CovidPerson` you can add or remove covid in the simulation. 

 1. ***Tune Behavioral Factors***
    * By turn on or off Vaccination agents’ immunity can change. Then it reduces the virus transmission
    * By changing `infectiousness` slider, you can change the virus transmission speed.

  1. ***Visualize Result***
     * By running model you can observe the colors changing of agents and understand the spread of infection
   
## Feature work on this model 
This model on shows above mention features. To make this model realistic,
* we can add When cases are confirmed, persons should be able to isolate or get quarantined, as well as get treated, while the turtles that represent such persons should disappear (NetLogo DIE) from the WORLD temporarily.
* And we can add vaccination procedure to specific agent not for everyone that make simulation more realistic.

## _References_

[^1]: https://ccl.northwestern.edu/2005/BlikAbrWil_IDC-05-demo.doc.pdf.
[^2]: https://www.netlogoweb.org/launch#http://ccl.northwestern.edu/netlogo/community/CoronaVirus.nlogo.
[^3]: https://www.netlogoweb.org/launch#http://ccl.northwestern.edu/netlogo/community/COVID-19%20Transmission%20Model.nlogo.
