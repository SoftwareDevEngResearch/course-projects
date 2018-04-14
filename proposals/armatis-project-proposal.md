# ME 599 Project Proposal
## Motivation
Many heat exchangers form hot spots due to varying heat fluxes or poor flow distribution. This is especially true in two-phase and extremely varied heat fluxes such as those seen in solar receivers. Hot spots can reduce performace and damage heat exchangers. Adjusting the flowrate based on the fluid temperature can reduce the surface temperatures due to increased convective heat transfer. Active PID control is quit helpful for this, especially for a small number of channels. However, with the increased use of microchannels, active control of every channel is cost prohibitive among many other problems. Thus, a passive control scheme is desired for many channels. A potential method of passive flow control based on temperature is by using bimetallic strips or shape memory materials to adjust an orifice hydraulic diameter based on the fluid temperature. This will in turn change the flowrate and thus the heat transfer rate in the channel and the surface temperature. This project will focus on modeling the transient effects of including an orifice outlet with a temperature depended hydraulic diameter.

## Functionality
This software will be used to understand the transient behaviour of different orifice designs. Most likely only I will be using it. This software will use heat transfer and pressure drop correlations to simulate the flowrate and temperature distribution as a function of the distance along the flow length and time. Multiple rectangular channels will be evaluated at once to understand the effects on the total flowrate and final mixed outlet temperature.

### Inputs
  * channel height, width, and length
  * overall pressure drop
  * 1D heat flux distribution along channel
  * inlet fluid temperature and pressure
  * fluid
  * orifice hydraulic diameter as a function of temperature
  * orifice mass, conductivity, and heat transfer coefficient
  * number of nodes
  * time step
  * total time domain length
  * tolerance

The orifice hydraulic diameter function and any other required detailed information  will be established using COMSOL or at the very least some basic principles of bimetallic strips or shape memory materials.

### Outputs
*All outputs are with respect to time*
  * 1D bulk fluid temperature distribution in each channel
  * 1D channel wall temperature distribution in each channel
  * orifice hydraulic diameters
  * individual channel and total mass flow rates
  * ratio of channel and orifice pressure drop for each channel

## Packages
  * CoolProp - for fluid properties as a function of temperature and pressure
  * Numpy - for faster computing

I may also use a SciPy solver or optimizer of some kind.


