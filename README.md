# Halley modeling
![a4](https://cdn.mos.cms.futurecdn.net/zzCKzkAndgXbTKNoKCUqu9-970-80.jpg.webp)

Halley's comet n-body modeling and simulation
## License: 
GNU General Public License v3.0
## Authors: 
- Juan Luis Ruiz Vanegas : juanluisruiz971@gmail.com
- David Calderon: dcc.david.calderon@gmail.com
- Cesar Arcos: racec9999@gmail.com
## Introduction: 
#### What is a comet?
>- Comets are remnants from the beginning of the solar system, about 4.6 billion years ago. They are balls of rock and ice that form tails as they approach the sun during their perfect elliptical orbits. When comets heat up, they eject gas and dust, forming a trail behind them. The sun illuminates this trail, making it glow.

Each comet has a small frozen part called a nucleus. The nucleus contains chunks of ice and frozen gases with bits of rocks and dust embedded in them. The nucleus may have a small rocky interior.
#### Halley comet
>- Halley is a short-period comet with origin in the so-called Kuiper belt beyond the orbit of Neptune. It has an orbit around the Sun with an approximate periodicity of 76 years, so it is said that the comet is seen only once in a lifetime; but, what would happen if it passed closer to the Earth? In the simulation we will make tests to present the results of this hypothesis with distance such as the moon and mars.

***
[Reference] (https://www.scientificamerican.com/espanol/imagenes-de-la-ciencia/ver-un-cometa-como-el-halley-ocurre-solo-una-vez-en-la-vida/) (http://solarsystem.nasa.gov/planets/profile.cfm?Object=Comets&Display=OverviewLong) (https://www.nationalgeographic.es/espacio/cometas-y-asteroides)
## Goals:
Our goal is to simulated the halley's comet trajectory with differents distance, which are mars distance and our main experiment moon distance, why the moon?, because is the closest body to earth.<br>
We hope to get realistic experiments for the near future be ready to destroy asteroids.
## Methodology
We follow the next points to resolve this problem:
1. Understanding the problem
 > Halley's comet has a trajectory that allows it to pass close to the Earth every 76 years. The conditions of distance from Earth, its weight, and its speed allow its orbit to be in equilibrium. But when does the equilibrium of the orbit break down and its trajectory gets closer to the Earth, at a distance equal to that of Mars or the Moon? Will the attractive force of the Earth be sufficient for Halley to impact with it?


2. Formulate hypotheses
>What would happen if a disturbance in Halley's orbit caused it to approach the Earth during its trajectory?
We hypothesize that with a closer distance (far distance equal to the Moon and Mars), the attractive force of the Earth will cause Halley's comet to modify its orbit, colliding with the Earth.

3. Define the type of model to be used
> We will simulate an n-body system with Halley and the Earth as particles on which gravitational attraction forces act.The force of attraction between two masses is directly proportional to the product of their masses and inversely proportional to the square of the distance between their centers. So as it says Newton's first law
that an object at rest will stay at rest, and an object in motion will stay in motion unless acted on by a net external force, therefore one of our particles will attract to the other affecting its orbit.

4. Define initial conditions
 > Described below
5. Perform modeling
  > Described below
6. Analyze results
  > Described below
7. Converge the model to a good 
modeling result.
  > Described below
## Initial variables:
* *dt* stands for delta-time, which is the time in seconds that elapses between integrations.
* All simulations were made using the Earth as a reference framework.
* The values of *dt* were selected empirically ensuring that each modeling converged to an expected result.
### Simulation 1 (Normal Distance)
* Reference: 
> The comet's closest approach to Earth occurred in 837: https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/ 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [30000,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,5e9,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
### Simulation 2 (Mars Distance)
* Reference:
> The minimum distance from Earth to Mars (2003): https://mars.nasa.gov/all-about-mars/night-sky/close-approach/ 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [30000,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,5.4e7,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
### Simulation 3 (Moon Distance)
* Reference:
> Average distance from Earth: https://www.space.com/18145-how-far-is-the-moon.html 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [30000,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,3.8e5,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 3.49
## Requirements:
* Python3 : `sudo apt-get install python3.8` 
* Matplotlib: `pip3 install mathplotlib`
* mpl_toolkits.mplot3d: `pip3 install mpl_toolkits`
## Installation:
- Clone the repository:
  > git clone https://github.com/M999X/Halley-modelling.git 
## Run:
Go to the folder of the project and and type on a console  `python3 normal_distance.py` to run the normal distance,`python3 mars_distance.py` for mars distance and `python3 moon_distance.py` for the moon, the program will be executed, and you will get a chart with the halley's trajectory.
## Results:
* All modeling, from the beginning to the end, contemplates a time span of 30 days.

* Simulation 1: Our first result show us that halley's comet pass far away of earth 5,097,768,243 kilometers to be precise, so do not affect the earth's orbit, in our chart we can watch neither the earth and halley's affects each other orbit, that's our expected results.<br>
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_normal_distance1.png)

* Simulation 2: We simulated the halley's comet with mars distance to earth 54.6 million kilometers , we can watch halley's comet create a kind of orbit with earth,originated by the Earth's attractive force. We also simulated with 7 months and halleys will crash into the earth, maybe if we add more particles to our model the comet will be attracted to other body.<br>

![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_mars_distance1.png)
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_mars_distance7.png)

* Simulation 3: We simulated the halley's comet with moon distance to earth 384,400 km , this chart show us a devastating news, if  halley's comet passes at the same distance that moon, will collide to earth causing the destruction of humanity.<br>
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_moon_distance1.png)
## Conclusion:
This modeling is important because it allows us to understand what happens with different initial conditions of Halley's Comet, such as its position with respect to the Earth, taking the Earth as a frame of reference. 

But what would happen if it passed closer to Earth?

As we could observe in the result of our second modeling, if the distance between both bodies (Earth and Halley) tends to reduce, Halley's velocity increases due to the attractive force that the Earth exerts on it.

In our third simulation, if the distance of the comet to the Earth is the same as the average distance between the moon and the Earth, Halley's comet will collide with the Earth.
The different results, caused by changes in the initial condition of the distances between the two bodies, are the result of the action of the Earth's attractive force on Halley's comet. The closer they are to each other, the stronger the Force of Attraction will increase.
This modeling is important because it allows us to understand what happens with different initial conditions of Halley's Comet, such as its position with respect to the Earth, taking the Earth as a frame of reference. 

* All modeling, from the beginning to the end, contemplates a time span of 30 days.

Our results from the first modeling show that the comet passes far away from the Earth and does not affect the Earth. This simulation was done with data from the comet's closest recorded approach to Earth, which occurred in 837, at a distance of 0.033 AU (3.07 million miles or 4.94 million kilometers). 

But what would happen if it passed closer to Earth?

In our second modeling, Our initial Halley-Earth distance conditions are the same as the Mars-Earth distance. Our results indicate that Halley's comet creates a kind of orbit around the Earth, originated by the Earth's attractive force. It also denotes that the comet has more velocity than the Earth.

In our third simulation, if the distance of the comet to the Earth is the same as the average distance between the moon and the Earth, Halley's comet will collide with the Earth.

The different results, caused by changes in the initial condition of the distances between the two bodies, are the result of the action of the Earth's attractive force on Halley's comet. The closer they are to each other, the stronger the Force of Attraction will increase.
Thanks to the universe for putting Halley's comet far away from the earth.

## Bibliography:
- https://ssd.jpl.nasa.gov/horizons.cgi
- https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/#:~:text=The%20comet's%20closest%20approach%20to,miles%20or%204.94%20million%20kilometers).
- https://en.wikipedia.org/wiki/Halley%27s_Comet
- https://theskylive.com/how-far-is-halley#:~:text=The%20distance%20of%20Comet%20Halley,equivalent%20to%2034.077709%20Astronomical%20Units.







