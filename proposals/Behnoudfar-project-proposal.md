Rapid Compression Machine (RCM): A Simulation

The purpose of this proposal is to develop a software package for simulating rapid compression machine (RCM) experiments. 
RCM is an experimental device used to simulate a single compression stroke of an internal combustion engine. It is often 
used for studying chemical kinetics of autoignition under idealized engine conditions. Accuracy of chemical kinetic models  
is fundamental to the development of new fuels. Typically, RCM experiments are conducted in order to acquire ignition delay 
data. The obtained ignition delay data is then compared to ignition delay data predicted by RCM simulations coupled with a 
chemical kinetic mechanism, in order to validate the mechanism [1].

The simplest way to model RCM experiments is by assuming an adiabatic, constant-volume process  with uniform condition [2]. 
However this method does not account for the heat loss from the test gases to the cold reaction chamber walls. Several 
approaches have been used by researchers to account for heat losses. Computational fluid dynamics (CFD) modeling is a very 
rigorous and accurate method but computationally expensive [1]. Other methods include the effective volume approach or an 
adiabatic core hypothesis approach [3]. These methods have drawbacks because they either require twice the amount of tests 
or are not accurate enough  for certain temperature sensitive experiments [1]. 

A computationally efficient, multi-zone model (MZM) [1] will be used in this work to improve the accuracy of RCM simulations 
and eliminate the need for non-reactive experiments. This model is one-dimensional, and splits the RCM into four main sub-models 
of the reaction chamber, gap, crevice volume, and the ringpack. The reaction chamber sub-model is split into multiple zones, to 
better model the boundary layer gas related to the adiabatic core hypothesis [3].

The components of proposed software will include modules for calculating the heat transfer, thermochemical state (temperature, 
pressure, volume, and species mass fractions) and ignition delay. Simulations of the RCM utilize the Closed Homogeneous Reactor 
model for each zone by specifying the initial conditions of the test, and by supplying the effective volume profile used to 
constrain the volume of the reactor. Chemical kinetics model, machine dimensions and choice of grid are other inputs to the 
software.

This work uses Cantera [4] for chemical kinetics simulations. Cantera is an open-source software library equipped with a built-in 
internal combustion engine model which accepts a polynomial function to describe piston velocity. Cantera solves the energy equation 
over a specified time interval to calculate system temperatures, pressure, and species concentrations. Scientific Python software 
tools including NumPy will also be used as appropriate.


 
[1] Wilson, David, and Casey Allen. "Application of a multi-zone model for the prediction of species concentrations in rapid 
compression machine experiments." Combustion and Flame 171 (2016): 185-197.

[2]  Niemeyer, Kyle E. "PyTeCK: a Python-based automatic testing package for chemical kinetic models." International Journal 
of Hydrogen Energy 32 (2007): 2216-2226. 

[3] Ezzell, Jenna. “An Analysis of Testing Variables in Rapid Compression Machine Experiments”. Diss. Marquette University, 2017.

[4] Goodwin, David G., Harry K. Moffat, and Raymond L. Speth. "Cantera: an object-oriented software toolkit for chemical kinetics,
thermodynamics and transport processes, 2009." URL http://www.cantera.org.
