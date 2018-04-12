Pavel Grechanuk Project Proposal

MCNP6 Input Deck Reader

MCNP6 is a general-purpose Monte Carlo N-Particle code that can be used for neutron, photon, electron, or coupled neutron/photon/electron transport. Specific areas of application include, but are not limited to, radiation protection and dosimetry, radiation shielding, radiography, medical physics, nuclear criticality safety, Detector Design and analysis, Fission and fusion reactor design, decontamination and decommissioning [1]. To validate the calculations of MCNP6, simulated results are compared against benchmark libraries that contain experimental measurements. This process forms the basis of a validation study to show area of applicability for an application of interest.

 Whisper was developed at Los Alamos National Laboratory (LANL) to automate, speed up and quantify in a defensible and reproducible way a significant portion of a validation study [2]. The data used in this study originates from 1,100+ benchmark cases in Whisper. My research is focused on applying machine learning methods to this dataset, in order to identify isotopes and reactions that are increasing the error of the calculation. The majority of that work is completed and currently under review for publication. The next stage of my research involves looking at how correlated my results are with the actual atomic densities of material present in the problems

The input decks to MCNP6 contain a lot of information about the problem like the materials present, the geometry, and the relative abundances of the materials. When working with hundreds of simulations it is difficult to quickly extract all of the important information from the problem for input analysis. Often the user is forced to write their own scripts that are specific to their application of interest.

This overarching goal of this project is to speed up this process by creating a general purpose tool to analyze MCNP6 input files. Using this package a user would quickly be able to see what isotopes are present in the various regions in the problem. This would be very useful to my research as often the abundances of various isotopes are varied across the different benchmarks. Additionally the package will be able to extract data of interest and output it for machine learning applications.


[1] Briesmeister, Judith F. MCNP--A general Monte Carlo code for neutron and photon transport. Los Alamos: Los   Alamos National Laboratory, 1986.

[2] Brown, Forrest B., Michael Evan Rising, and Jennifer Louise Alwin. MCNP-WHISPER Methodology for Nuclear Criticality Safety Validation. No. LA-UR--16-23757. Los Alamos National Lab.(LANL), Los Alamos, NM (United States), 2016.
