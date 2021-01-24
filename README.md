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
> In this project we will make the simulation of Halley's comet passing near the Earth over a month. It has an orbit around the Sun with an approximate periodicity of 76 years, so it is said that the comet is seen only once in a lifetime; but, what would happen if it passed closer to the Earth? In the simulation we will make tests to present the results of this hypothesis.
***
[Reference] (https://www.scientificamerican.com/espanol/imagenes-de-la-ciencia/ver-un-cometa-como-el-halley-ocurre-solo-una-vez-en-la-vida/)

## Methodology
We follow the next points to resolve this problem:
1. Understanding the problem
2. Formulate hypotheses
3. Define the type of model to be used
4. Define initial conditions
5. Perform modeling
6. Analyze results
7. Converge the model to a good modeling result.
## Initial variables:
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6x10^24 kg
  * Orbital speed: 30 km/sec
* Halley's Comet:
  * Position: [0,5e9,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: 54.5 km/sec
## Requirements:
* Python3 : `sudo apt-get install python3.8` 
* Matplotlib: `pip3 install mathplotlib`
* mpl_toolkits.mplot3d: `pip3 install mpl_toolkits`
## Installation:
- Clone the repository:
  > git clone https://github.com/M999X/Halley-modelling.git 
## Run:
Go to the folder of the project and and type on a console  `normal_distance.py` to run the normal distance,`mars_distance.py` for mars distance and `moon_distance.py` fotrthe moon, the program will be executed, and you will get a chart with the halley's trajectory.
## Results:
* Simualtion 1: Our first result show us that halley's comet pass far away of earth, so do not affect the earth's orbit, in our chart we can watch neither the earth and halle's affects each other orbit, thaths our expected results
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_normal_distance.png)
* Simulation 2: We simulated the halley's comet with mars distance to earth, we can watch halley's comet create a kind of orbit with earth, we need to simulate it with more time to know how to end this orbit.
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_mars_distance.png)
* Simulation 3: We simulated the halley's comet with moon distance to earth, this chart show us a devastating news, if  halley's comet pass at the same distance that moon, will colide throught earth causing the destruction of the humanity.
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_moon_distance.png)
## Conclusion:
Our results show comet pass far away of earth and do not affect earth.The comet's closest approach to Earth occurred in 837, at a distance of 0.033 AU (3.07 million miles or 4.94 million kilometers). But, what would happen if pass closer to earth ?.
If pass at the same distance as mars, halley's comet create a kind of orbit and the comet have more velocity than earth.
If pass at the same distance as the moon, halley's comet will collide with earth. 
Thanks to the universe to put halley's comet far away the earth.  
## Bibliography:
- https://ssd.jpl.nasa.gov/horizons.cgi
- https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/#:~:text=The%20comet's%20closest%20approach%20to,miles%20or%204.94%20million%20kilometers).
- https://en.wikipedia.org/wiki/Halley%27s_Comet

