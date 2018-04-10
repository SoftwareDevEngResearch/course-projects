I previously worked on analyzing the impact of spatial homogenization for the 
Experimental Breeder Reactor II (EBR-II). This work included utilizing software
from a doctoral student called MICKA (MCNP Input Card and Kcode Architect). 
This program was built to aid in the development of input files a 
for the EBR-II benchmark project, of which over 100 input files were required
and the input files were over 100,000 lines long. When I entered the project,
MICKA was nearly complete and I built in multiple functions to spatially 
homogenize regions of the core to determine their impact. MICKA was programmed
in MATLAB, and required extensive usage of excel documents for the input 
parameters. This made MICKA a singular use tool. Although it could be 
retrofitted to perform other benchmark designs of a similar nature, much of the
data was spread out over 10-20 excel documents. This meant the probability of
inducing some type of error would be quite high where it to be changed. I wrote
a paper discussing the work, it is currently unpublished, but can be seen upon
request.

The MICKA project introduced me to the use of programming to assist in the 
creation of input files for programs such as MCNP. The ability of a computer 
to create multiple variations of input files, with relative ease, will allow 
my current research to progress much quicker than is currently possible. My 
current work utilizes MCNP to examine the impact that materials, geometry, and 
data libraries have on reactor parameters such as the multiplication factor,
fraction of delayed neutrons, and the energy spectrum. This requires 
building a plethora (100+) of MCNP input files, where each file is slightly 
different, however those difference can impact various other input 
parameters. Due to this, my project will be to create a generalized MCNP input
deck for fast reactor geometries. This projects name will be FRIDG (Fast Reactor
Input Deck Generator), and the first phase will build fast reactor assemblies.
This phase will be the goal of the ME 599 project. After this phase however,
it is my hope to expand FRIDG to create a full fast reactor core.

The creation of a reactor assembly falls into three categories: materials, 
geometry, and problem data. The focus of this project will be to generate an
MCNP input card from user defined data. Ideally, it will be a GUI, however, 
that may be pushed off until a later date. The user will be able to define 
materials that will be used in the problem, and FRIDG will take those materials
and create a material card. The user will also be able to define the specific 
geometries for the fuel assembly, such as the fuel pin diameter, fuel pin
height, number of fuel pins per assembly, etc. Again, FRIDG will take these 
parameters and build the associated geometry in an MCNP format. It will then
take the materials defined, and applying those materials to the given geometry
in question. The last step is to incorporate any user defined data, such as
tallies (information regarding the problem set), physical phenomena, and
the specifics for the criticality measurements. The major difference I hope 
to accomplish with FRIDG is to provide the fast reactor community with a 
resource that can quickly and accurately create general fast reactor MCNP
input files.

Currently, the extent of dependencies is not well known, but some have been
identified. The first, and most important, will be the use of numpy for 
array manipulation and usage. Along with this, there is a potential to use
pandas for additional data structures, however I am currently unfamiliar with
pandas abilities and limitations. Further down the line (it probably won't
occur in this class) I would like to incorporate a GUI using Tkinter for an
easier user format. Along with this, I would eventually like to incorporate 
modules which can graph outputs such as pin power, energy distribution, and 
flux values (which would require Matplotlib). These modules could also 
incorporate the ability to read large amounts of output files and grab 
specific values to allow for comparison between different runs.
