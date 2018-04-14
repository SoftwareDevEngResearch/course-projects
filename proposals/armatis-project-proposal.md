# ME 599 Project Proposal
## Motivation
Many heat exchangers form hot spots due to varying heat fluxes or poor flow distribution. This is especially true in two-phase and extremely varied heat fluxes such as those seen in solar receivers. Hot spots can reduce performace and damage heat exchangers. Adjusting the flowrate based on the fluid temperature can reduce the surface temperatures due to increased convective heat transfer. Active PID control is quit helpful for this, especially for a small number of channels. However, with the increased use of microchannels, active control of every channel is cost prohibitive among many other problem. Thus, a passive control scheme is desired for many channels. A potential method of passive flow control based on temperature is by using bimetallic strips or other shape memory materials to adjust an orifice hydraulic diameter flow based on the fluid temperature. This will in turn change the flow rate and thus the heat transfer rate in the channel and the surface temperature. This project will focus on modeling the transient effects of including an orifice outlet with a temperature depended hydraulic diameter.

## Functionality
This software will be used understand the transient behaviour of different orifice designs. Most likely, only I will be using it. This software will use heat transfer and pressure drop correlations to simulate the flow rate and temperature distribution as a function of the distance along multiple rectangular channels and time.

### Inputs
  * channel dimensions (height, width, and length)
  * overall pressure drop
  * heat flux distribution along channel (1D)
  * inlet conditions (temperature and pressure)
  * fluid name
  * orifice hydraulic diameter as a function of temperature and time
  * number of nodes
  * time step
  * total time to simulate
  * tolerance

### Outputs
*All outputs are with respect to time*
  * bulk fluid temperature distribution in each channel (1D)
  * channel wall temperature distributions (1D)
  * orifice hydraulic diameters
  * individual channel and total mass flow rates
  * ratio of channel and orifice pressure drop for each channel

The orifice hydraulic diameter function will be established using COMSOL or at the very least some basic principles of bimetallic strips or shape memory materials. 

## Packages
  * CoolProp - for fluid properties as a function of temperature and pressure
  * Numpy - for faster computing time

I may also use a SciPy solver or optimizer of some kind.


