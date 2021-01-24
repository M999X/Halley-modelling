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
> In this project we will make the simulation of Halley's comet passing near the Earth. It has an orbit around the Sun with an approximate periodicity of 76 years, so it is said that the comet is seen only once in a lifetime; but, what would happen if it passed closer to the Earth? In the simulation we will make tests to present the results of this hypothesis.
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
  * Position: [0,4.93e9,0]
  * Mass: 2.2×10^14 kg
  * Orbital speed: 54.5 km/sec
## Requirements:
* Python3 : <pre><code> sudo apt-get install python3.8 </code></pre>
* Matplotlib: 'pip3 install mathplotlib'
* mpl_toolkits.mplot3d: 'pip3 install mpl_toolkits'
## Installation:
- Clone the repository:
  > git clone https://github.com/M999X/Halley-modelling.git 
## Run:
- python3 n-body.py
## Results:
![Test Image 4](https://github.com/M999X/Halley-modelling/blob/main/Results/Modelo-Geocentrico.png)
## Conclusion:
## Software tools:
## Bibliography:
- https://ssd.jpl.nasa.gov/horizons.cgi
- https://solarsystem.nasa.gov/asteroids-comets-and-meteors/comets/1p-halley/in-depth/#:~:text=The%20comet's%20closest%20approach%20to,miles%20or%204.94%20million%20kilometers).
- https://en.wikipedia.org/wiki/Halley%27s_Comet
