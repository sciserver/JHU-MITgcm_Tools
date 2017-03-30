# Welcome to the SciServer Ocean Modelling User Case

[SciServer](http://www.sciserver.org/) consists of integrated tools that work together to create a full-featured system.
SciServer is administrated by The Institute for Data Intensive Engineering and Science (idies) and The Johns Hopkins University, and is funded by National Science Fundation award ACI-1261715.

The Ocean Modelling User Case consists of a set of tools that provide access to numerical models outputs resulting from high resolution Ocean General Circulation Models (GCMs) set up and run by [Prof. Thomas W. N. Haine](http://sites.krieger.jhu.edu/haine/) group (Johns Hopkins University - Department of Earth and Planetary Sciences).

## Getting started

### SciServer
1. [Register for a new SciServer account](http://portal.sciserver.org/login-portal/Account/Register) or [Log in to an existing SciServer account](http://portal.sciserver.org/login-portal/Account/Login?callbackUrl=http:%2f%2fcompute.sciserver.org%2fdashboard)
2. Create a new container and choose:
```markdown
- Image: MATLAB R2016a
- Public Volumes: Ocean Circulation
```
3. Click on the green play button.

The workspace contains:
```markdown
- OceanCirculation: Read only directory containing data.
- scratch: Personal directory for storing large temporary files and output.
- persistent: Personal directory for long-term storage of relatively small files.
```

### MITgcm tools
1. Open a new terminal (_New_ -> _Terminal_).
2. Clone the MITgcm tools (e.g. into the persistent directory):
```sh
$ cd /home/idies/workspace/persistent
$ git clone https://github.com/malmans2/JHU-MITgcm_Tools.git
```
3. Get the latest available version:
```sh
$ cd /path/of/MITgcm_Tools
$ git pull
```
[JHU-MITgcm_Tools](https://github.com/malmans2/JHU-MITgcm_Tools) contains:
```markdown
- code: Directory containing matlab scripts and functions. Type help function.m in matlab to get more details.
  - eulerian: Subdirectory containing eulerian tools.
  - lagrangian: Subdirectory containing lagrangian tools (particle tracking code - not available yet).
- info: Directory containing description and list of available variables for each experiment.
- notebooks: Directory containing notebooks templates that walk you through how to use our tools.
```


## Example
1. Log in to SciServer and open a container.
2. Open a terminal (_New_ -> _Terminal_), create a new directory and open it:
```sh
$ mkdir /home/idies/workspace/persistent/Test
$ cd /home/idies/workspace/persistent/Test
```
3. Copy a notebook template into the _Test_ directory:
```sh
$ cp  /path/of/MITgcm_Tools/notebooks/eulerian_template.ipynb mynotebook.ipynb
```
4. Open your notebook (click on _persistent_ -> _Test_ -> _mynotebook.ipynb_)
5. Now you can edit and run the notebook following the comments (you can NOT delete the first cell because it sets the environment). You can use the menu/toolbar, or you can run a single cell by selecting it and pressing Shift+Enter. Jupyter prints the outputs below every cell only when the script contained in that cell is done. If you want to monitor the progress of your notebook, use the logfile option in the first cell: e.g. set `logname = ['logfile'];` and read it through the terminal:
```sh
$ tail -f logfile
```
Once you get familiar with our tools, you can easily build your own notebooks using the scripts/functions contained in [JHU-MITgcm_Tools/code](https://github.com/malmans2/JHU-MITgcm_Tools/tree/master/code).

### How to cite us:
#### To cite our dataset, please use this reference: 
Almansi et al., in progress

#### To cite our Lagrangian Tracking Particle Code, please use this reference: 
R. Gelderloos, A. S. Szalay, T. W. N. Haine and G. Lemson, "A fast algorithm for neutrally-buoyant Lagrangian particles in numerical ocean modeling," 2016 IEEE 12th International Conference on e-Science (e-Science), Baltimore, MD, 2016, pp. 381-388.
doi: 10.1109/eScience.2016.7870923
keywords: {ecology;marine systems;numerical analysis;oceanography;statistical analysis;vectors;3D along-boundary flow field;Lagrangian analysis;fast algorithm;fast particle-tracking algorithm;large-scale oceanic phenomena;multitime scale oceanic phenomena;neutrally-buoyant Lagrangian particles;numerical ocean modeling;numerical ocean simulations;parallelized;particle trajectories;simulated flow kinematics;solid boundary particle sliding;vectorized;Analytical models;Computational modeling;Graphics processing units;Interpolation;MATLAB;Oceans;Trajectory},
URL: [http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7870923&isnumber=7870873](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7870923&isnumber=7870873)


### Support or Contact
Mattia Almansi: mattia.almansi@jhu.edu
Dr. Renske Gelderloos:  rgelder2@jhu.edu 

Having trouble with JHU-MITgcm_Tools or JHU-MITgcm_Tools? Contact us and we’ll help you!
The [SciServer support page](http://www.sciserver.org/support/) may be useful.
JHU-MITgcm_Tools is open source: let us know if you find any bugs or if you want to share any notebooks/functions.





