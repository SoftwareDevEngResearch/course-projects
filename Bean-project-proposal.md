



# Calibration Suite for Infrared Thermography Devices

## Background

Calibration of infrared thermography devices such often a tedious and time consuming process that is critical for successful research. Calibrations are especially important for Infrared cameras since the response of the detector is highly dependent on the physical attributes of the device configuration and environmental variables. Factors that affect camera calibrations include but are not limited to the following variables:

* Distance from the camera to the radiation source
* Transmissivity of optics and filters
* Uniformity of the blackbody
* Humidity, temperature and composition of intermediate participating medium 
* Non uniformity of detector response 
* Choice of region of interest (ROI) during calibration 
* Sensor integration time
* Settings of lenses (f-stop etc.)


This software package aims to streamline current methodologies, reduce the learning curve and increase the consistency of IR device calibration. Streamlining will be accomplished by aggregating and standardizing the process into a single program of central area since in the past this has been a distributed process involving multiple pieces of software with each user coming up with there own method. Streamlining and standardizing this process will also decrease the learning curve of the calibrations as well as reduce the propensity for error in new users. Users of this software tool would be those that conduct research or measurements requiring blackbody calibrations of IR cameras.

## Functionality

In order to condense the blackbody calibration into one software package the software will have to interface across multiple different languages and packages. The tasks that the software will have to perform are as follows

#### Interface with the blackbody

The software must interface with the blackbody in order to control the temperature of the cavity according to the calibration schedule. A cool down process will also have to be conducted to prevent damage to the device. The blackbody interface is conducted through an RS232 interface. This control will likely be done in C with the Python writing and compiling the C code according to user inputs unless a purely Python communication solution can be found. This control functionality will eliminate the need for a person to manually adjust the blackbody every time the temperature needs to be changed.

#### Interface with the IR camera

The software will have to acquire images from the camera as well as control the settings of the camera to match the experimental conditions. The camera connects through a Gigabit Ethernet (GigE) interface for acquisition and control. 

#### Image analysis

#### Photon counts vs intensity curve generation

#### Non Uniformity Correction (NUC)

## Packages and Integrations

The following packages and integrations are anticipated for this project

* RADCAL (participating environmental medium correction)

* C (interfacing with the blackbody controller)

* OpenCV (interfacing with the camera using GigE Vision)

* NumPy

* PIL

* SciPy

* Scikit-image

## Building off of previous work

  ​

  ​

## References 



## Instructions

Add the file in the proposals folder, and commit this addition
Push the change to your version of the repo (git push)
On your repo at GitHub, submit a new pull request back to the original “upstream” repo.

Please describe the functionality of your intended software project, including who might use it. This includes what the software will actually do—will it simulate something, process data, or something else?—the overall components you expect to design, and expected inputs/outputs.
Most packages should build on some existing methodology, so cite papers as appropriate. Also describe how this builds on any prior work you've done, if relevant. Make it clear how this software package will be different from existing work (yours or otherwise).
Proposals should be one or two pages long.