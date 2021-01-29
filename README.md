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
>- Halley is a short-period comet with origin in the so-called Kuiper belt beyond the orbit of Neptune. It has an orbit around the Sun with an approximate periodicity of 76 years, so it is said that the comet is seen only once in a lifetime; but, what would happen if it passed closer to the Earth? In the simulation we will make tests to present the results of this hypothesis with distance such as the moon,mars and a crash distance.

***
[Reference] (https://www.scientificamerican.com/espanol/imagenes-de-la-ciencia/ver-un-cometa-como-el-halley-ocurre-solo-una-vez-en-la-vida/) (http://solarsystem.nasa.gov/planets/profile.cfm?Object=Comets&Display=OverviewLong) (https://www.nationalgeographic.es/espacio/cometas-y-asteroides)
## Goals:
Our goal is to simulated the halley's comet trajectory with differents distance, which are mars distance, moon distance and our main experiment the crash distance 3e6, why 3e6?. For the reason that PHOs is one of the closest bodies  have a minimum orbital intersection distance of less than 0.05 au, about 7.5 million km from the Earth’s orbit, measuring more than 140 metres across. An object of this size is large enough to cause devastation on a regional scale with possible global consequences. Therefore imagine the devastation on the planet if Halley’s comet is attracted by earth.<br>
We hope to get realistic experiments for the near future be ready to destroy asteroids.
## Methodology
We follow the next points to resolve this problem:
1. Understanding the problem
 > Halley's comet has a trajectory that allows it to pass close to the Earth every 76 years. The conditions of distance from Earth, its weight, and its speed allow its orbit to be in equilibrium. But when does the equilibrium of the orbit break down and its trajectory gets closer to the Earth, at a distance equal to that of Mars or the Moon? Will the attractive force of the Earth be sufficient for Halley to impact with it?

2. Formulate hypotheses
>What would happen if a disturbance in Halley's orbit caused it to approach the Earth during its trajectory?
We hypothesize that with a closer distance (far distance equal to the Moon and Mars or nearest), the attractive force of the Earth will cause Halley's comet to modify its orbit, colliding with the Earth.

3. Define the type of model to be used
* We will use a simulation system of n-bodies of particles under the influence of the Force of Attraction of the particles involved in the system. In this case Halley and the Earth will be those particles on which Gravitational attraction forces act.
Our simulation is a direct N-body gravitational simulation. Our equations of motion under the influence of mutual gravitational force are integrated numerically.

> Force of Attraction (Gravitational Force)
Two bodies, by the fact of having mass, experience a force of attraction towards other bodies with mass.
The force of attraction between two masses is directly proportional to the product of their masses and inversely proportional to the square of the distance between their centers. So as Newton's first law says that an object at rest will remain at rest, and an object in motion will remain in motion unless acted upon by a net external force, therefore one of our particles will attract the other affecting its orbit.

4. Define initial conditions
 > Described below
5. Perform modeling
  > Described below
6. Analyze results
  > Described below
7. Converge the model to a good 
modeling result.
  > Described below
## Initial conditions:
* *dt* stands for delta-time, which is the time in seconds that elapses between integrations.
* All simulations were made using the Earth as a reference framework.
* The values of *dt* were selected empirically ensuring that each modeling converged to an expected result.
### Simulation 1 (Normal Distance)
* Reference: 
> The comet's closest approach to Earth occurred in 837: https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/ 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,4.93e9,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
### Simulation 2 (Mars Distance)
* Reference:
> The minimum distance from Earth to Mars (2003): https://mars.nasa.gov/all-about-mars/night-sky/close-approach/ 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,54.6e9,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
### Simulation 3 (Moon Distance)
* Reference:
> Average distance from Earth: https://www.space.com/18145-how-far-is-the-moon.html 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,3.84e8,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
### Simulation 4 (Attract Impact)
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,3e7,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
### Simulation 5 (Crash Distance)
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Halley's Comet:
  * Position: [0,3e6,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 60
## Requirements:
* Python3 : `sudo apt-get install python3.8` 
* Matplotlib: `pip3 install mathplotlib`
* mpl_toolkits.mplot3d: `pip3 install mpl_toolkits`
## Installation:
- Clone the repository:
  > git clone https://github.com/M999X/Halley-modelling.git 
## Run:
Go to the folder of the project and and type on a console  `python3 normal_distance.py` to run the normal distance, `python3 mars_distance.py` for mars distance,`python3 moon_distance.py` for moon distance, `python3 attract_distance.py` for attraction distance, and `python3 crash_distance.py` for the crash into earth, the program will be executed, and you will get a chart with the halley's trajectory.
## Results:
* All modeling, from the beginning to the end, contemplates a time span of 1 month.

* Simulation 1 (Mars Distance): Our first result shows that if Halley passes at a distance equal to that of Mars, the force of attraction to the Earth will not be sufficient to notice a significant change in its orbit.<br>
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_mars_distance1.png)

* Simulation 2 (Normal Distance): In the simulation where Halley is at the closest recorded distance, there are no changes in its orbit due to the attractive force exerted on it by the Earth.<br>

![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_normal_distance1.png)


* Simulation 3 (Moon Distance): In the simulation in which Halley is at the average distance of the Moon, no considerable perturbations are perceived in its orbit.<br>
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_moon_distance1.png)

* Simulation 4 (Attract Impact):
In the fourth simulation, we bring Halley's comet to a distance one order of magnitude closer to the Earth, and here the impact of the Earth's attractive force on the comet is already noticeable, modifying its orbit considerably.
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_attract_distance1.png)
* Simulation 5 (Crash Distance):
In our latest simulation we lowered our simulation by one more order of magnitude and, unlike the previous one, this distance is sufficient to attract Halley to a point where it would collide with the Earth.
![Test Image 5](https://github.com/M999X/Halley-modelling/blob/main/Results/Simulation_crash_distance1.png)

## Conclusion:
This modeling is important because it allows us to understand what happens with different initial conditions of Halley's comet (its position with respect to the Earth), taking the Earth as a frame of reference.

This model allows us to answer the question What would happen if Halley's orbit were perturbed and its distance from the Earth changed?

The different results, caused by changes in the initial condition of the distances between the two bodies, are the result of the action of the attractive force of the Earth on Halley's comet. The closer they are to each other, the stronger the attractive force. 
At the end of simulation 3 nothing happened so we decided to create an hypothetical case with a smaller distance 3e6 in this case we could to recreate a new extinction.
At the end we noticed the importance of modeling and simulation  as well as The International Asteroid Warning Network (IAWN) which also performs observations, orbit computation, modelling and other scientific research related to the impact potential and effects of asteroids on the Earth.
Thanks to the universe for having put Halley's comet far away from the Earth.





## Bibliography:
- https://ssd.jpl.nasa.gov/horizons.cgi
- https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/#:~:text=The%20comet's%20closest%20approach%20to,miles%20or%204.94%20million%20kilometers).
- https://en.wikipedia.org/wiki/Halley%27s_Comet
- https://theskylive.com/how-far-is-halley#:~:text=The%20distance%20of%20Comet%20Halley,equivalent%20to%2034.077709%20Astronomical%20Units.
- https://www.unoosa.org/oosa/en/ourwork/topics/neos/index.html#:~:text=A%20near%2DEarth%20object%20is,kilometres%2C%20of%20the%20Earth's%20orbit.






