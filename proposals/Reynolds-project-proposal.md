# A Python Package for Nodal Quasi-Diffusion Methods
##### Aaron J Reynolds

I intend to build a software package to solve the neutron transport equation using 
nodal quasi-diffusion (NQD) methods. A solution to the neutron transport equation describes 
the neutron population across the problem of interest. As neutrons are responsible for 
initiating the fission process in fission reactors, this population distribution is of 
great interest when analyzing a reactor core.

I will use this software package throughout my research, and I expect other graduate 
students or researchers in the computational field may use it, too. 

#### Nodal Quasi-Diffusion Methods

Nodal diffusion methods are used to perform the majority of reactor analysis for 
commercial nuclear power plants. These methods have found such wide application 
because the necessary computations are of low cost. [1] Typically, with these methods, one 
works with the neutron diffusion equation, an approximation to the neutron transport 
equation found after making many assumptions. In these assumptions, some of the transport 
effects are lost. 

The quasi-diffusion equation, shown below, is also an approximation to the neutron transport 
equation, but it is formulated in such a way as to preserve transport effects through 
the calculation of an Eddington factor. [2] The quasi-diffusion equation can also more 
readily incorporate multiphysics phenomena compared to the standard diffusion 
equation. 

<p align="center">
<img src="https://github.com/aaronjamesreynolds/ajr/blob/master/qd.JPG" height="70">  where <img src="https://github.com/aaronjamesreynolds/ajr/blob/master/eddington.JPG" height="90"> 
</p>

NQD methods, then, benefit from the low cost of computation 
inherent in nodal diffusion methods, while also preserving transport effects by 
incorporating quasi-diffusion constraints. In my future research, I hope to apply these methods to next-generation
reactor design analysis, where certain multiphysics phenomena must be considered. 

#### Functionality

The NQD software package will do a number of things:

1. Read in heterogeneous problem data. 
2. Calculate a heterogeneous flux solution with the neutron transport equation. (Using the step characteristic method)	
3. Use heterogeneous flux to calculate Eddington factors and homogenized data.
4. Formulate the homogenized problem.	
5. Build the linear system for NQD.
6. Use power iteration to converge on a homogenized flux. 

The inputs will be the heterogeneous material properties of the problem, and the output will be a 
transport solution to the problem with homogenized data. Below is a flowchart of the NQD solver.

<p align="center">
<img src="https://github.com/aaronjamesreynolds/ajr/blob/master/flowchart.JPG"> 
</p>

#### Current State

I have built a few of the above components in Matlab. In their present state, they are 
very clumsy, unorganized, and would benefit greatly from an object-oriented 
implementation. A Python implementation would also be more compatible with other work 
in the field.

#### Package Dependence

I plan to use Numpy extensively.

#### References

[1] Lawrence, R.D. "Progress in Nodal Methods for the
Solution of the Neutron Diffusion and Transport Equations."
Progress in Nuclear Energy. 1986; Vol. 17, No. 3, pp. 271-301.

[2] Hitaru, H. "Advanced Computational Methodology for
Full-Core Neutronics Calculations." Dissertation. 2004.

