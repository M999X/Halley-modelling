# Halley modeling
![a4](https://cdn.mos.cms.futurecdn.net/zzCKzkAndgXbTKNoKCUqu9-970-80.jpg.webp)
Halley's comet n-body modeling and simulation
### Afiliación
![https://upload.wikimedia.org/wikipedia/commons/7/79/LOGO-COMPUESTO-UNAM-ENES_-_copia.png](https://user-images.githubusercontent.com/28678081/106318209-2e080b80-6235-11eb-944f-4d40f52ecedb.png)                
Somos estudiantes de 5to semestre (al momento de edición) de la Licenciatura Tecnologías para la Información en Ciencias impartida en la Escuela Nacional de Estudios Superiores, UNAM, Unidad Morelia.
## License: 
GNU General Public License v3.0
## Authors: 
- Juan Luis Ruiz Vanegas : juanluisruiz971@comunidad.unam.mx
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
## Goals 
Our goal is to simulate Halley's orbit and the Moon's orbit around the Earth in a 3-body system consisting of the Earth, the Moon and Halley. 
## Requirements:
* Python3 : `sudo apt-get install python3.8` 
* Matplotlib: `pip3 install mathplotlib`
* mpl_toolkits.mplot3d: `pip3 install mpl_toolkits`
## Installation:
- Clone the repository:
  > git clone https://github.com/M999X/Halley-modelling.git 
## Run:
>python3 normal_distance.py

## Methodology
We follow the next points to resolve this problem:
1. Understanding the system
 > Halley's comet has a trajectory that allows it to pass close to the Earth every 76 years. The conditions of distance from Earth, its weight, and its speed allow its orbit to be in equilibrium. In addition, the Moon has an orbit around the Earth with a period of 29 days.

2. Formulate hypotheses
>If our modeling is in equilibrium, we will be able to model the trajectory of both orbits around the Earth in a 30-day period.

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
### First Modeling, make the system converge to the Moon's orbit around the Earth.

Our first simulation focused on making sure that our model converged with two bodies, the Moon and the Earth, since its orbit is relatively close to Halley's, so the computational cost to converge it and find the dt is lower.
* Reference:
> Average distance from Earth: https://www.space.com/18145-how-far-is-the-moon.html 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Moon:
  * Position: [0,3.84e8,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 1.1 s

### Modeling 2 (Including the three bodies)
In the second model, we have the three bodies that are part of our system. In this one, we will model Halley with the closest distance to Earth on record; and the Moon with the average distance.

* Reference: 
> The comet's closest approach to Earth occurred in 837: https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/ 
* Earth: 
  * Position: [0, 0, 0]
  * Mass: 6 x 10^24 kg
  * Orbital speed: [0,0,0] 30 km/sec
* Moon:
  * Position: [0,3.84e8,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* Halley's Comet:
  * Position: [0,4.93e9,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: [54500,0,0] 54.5 km/sec 
* dt = 1.1 s

## Results:
* All modeling, from the beginning to the end, contemplates a time span of 1 month.

* Modeling 1 (Earth and Moon): 
It is observed that the Moon's orbit is closed, converging to an ellipse.
![Moon Orbit](https://github.com/M999X/Halley-modelling/blob/main/Results/Moon_Orbit_Simulation_30_days.png)
<br>

* Modeling 2 (three bodies): Modeling with the three bodies allows us to observe the scales of the distances at which Halley and the Moon are located. As far as the Moon is concerned, it can be confusing when looking at its orbit, but what is happening is that the scales of the y-axis and the x-axis are different. One is on scale e^9 and the other is on scale e^11.We canWe can see that the Moon's orbit is maintained and, furthermore, that we can simulate Halley's orbit.
<br>

![three bodies](https://github.com/M999X/Halley-modelling/blob/main/Results/Halley_Moon_Earth/Normal_Distance.png)

## Conclusion:
We can see that the modeling for Halley's orbit is correct. In addition, it allows us to contrast its closest recorded distance with the Moon's distance from the Earth.





## Bibliography:
- https://ssd.jpl.nasa.gov/horizons.cgi
- https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/#:~:text=The%20comet's%20closest%20approach%20to,miles%20or%204.94%20million%20kilometers).
- https://en.wikipedia.org/wiki/Halley%27s_Comet
- https://theskylive.com/how-far-is-halley#:~:text=The%20distance%20of%20Comet%20Halley,equivalent%20to%2034.077709%20Astronomical%20Units.
- https://www.unoosa.org/oosa/en/ourwork/topics/neos/index.html#:~:text=A%20near%2DEarth%20object%20is,kilometres%2C%20of%20the%20Earth's%20orbit.






