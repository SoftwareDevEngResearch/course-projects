# ME-599 Project Proposal
### Matthew Morse

This proposal is for a software package to assist in the design of cost-effective spin stabilization mechanisms for small launch vehicles. Inspired by work at NASA Marshall Space Flight Center, the goal of the software package will be to solve differential equations of motion of a rocket that is in space or vacuum-like conditions with different design parameters. Specifically, commercially available solid motors can be used as a cost-effective option for spin-stabilization. Crucial parameters for flight stability include motor sizing, placement, and burn characteristics because these motors are not able to be throttled.

A software package than can simulate a rocket's flight in the specified conditions for spin-up will prove to be a useful design tool. There will be several inputs into the program because of the uniqueness of each design iteration. The inputs will include

* physical design characteristics of the launch vehicle including
	* roll, pitch, and yaw moments of inertia
	* radial and longitudinal location of spin-up motors
* ignition delay between two motors
* simulation duration
* the solid rocket motor selected for analysis and thrust data from [thrustcurve.org](http://www.thrustcurve.org/)

Some of the desired outputs of the program include

* Eulerian angle time profiles
* nutation angle time profile and maximum nutation angle
* the path of the rocket's longitudinal axis
* a simple animation of the rocket's flight (if time permits)

To reiterate, the purpose of the software package is to provide a designer with a first pass analysis of rocket stability with a few selected design parameters. The maximum tolerable nutation angle is a predetermined design constraint that must be met and this simulation will reveal whether or not a set of design characteristics produces a stable flight. The intended users for this software package will be project leads in Marshall Space Flight Center's ER-50 Solid Propulsion Division as well as student researchers and interns who will contribute to the development of cost-effective small launch vehicles.

To successfully implement the proposed software package, there are a few components to be designed. First, a scraper script may need to be implemented that is able to pull data from [thrustcurve.org](http://www.thrustcurve.org/) to be used in the simulation. Alternatively, the data could also be pre-downloaded and stored as a library of data files. Second, a script that solves the system of differential equations that describe the rocket's flight is necessary. Third, the simulation data should be plotted for visualization purposes. Finally, because of the numerous inputs, a graphical user interface would be beneficial to design if time permits.

Although a simple simulation package for this particular application does not exist, there have been other developments that simulate similar motion. For example, Kareem Omar and Michael Briggs developed a simulation for CubeSat stabilization [1]. Their simulation simulated satellite trajectories and orientations allowing the end user to experiment with different satellite geometries. While their package requires more physical models (i.e. atmospheric models) than the simplified proposed model for rocket spin-stabilization, the underlying concepts are similar. Although Omar and Briggs did not utilize python to develop their software package, parallels can be drawn between their methods and the desired functionality of the proposed software package. Specifically, I would expect the proposed software package to depend on the following python packages: numpy, scipy/odeint, and matplotlib. As development progresses, this list may expand.

Towards the end of my time at MSFC, I attempted to implement a similar program in MATLAB. However, it was never seen to completion, was filled with bugs, and had poor performance. As a result, successive interns have attempted to fix the issues with no success. By revisiting this problem, the goal is to correctly implement the package so that it is reusable by others. Addtionally, spin-stabilization is generally accomplished by systems that can be throttled. Using solid propellant for spin-stabilization is a novel task and provides cost benefits as well as a reduction complexity compared to liquid/gaseous counterparts.

### References

[1] Omar, Kareem, and Michael Briggs. "Simultaneous Orbital and Attitude Propagation of CubeSats in Low Earth Orbit." (2016).
