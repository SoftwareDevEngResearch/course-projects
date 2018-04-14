Name: Makenzie Brian
Class: ME 599
File: Project Proposal

This project is intended to take a thermal camera image and segment out the heat sources from the other parts of the image. This will be used in the Ebola that is project currently in progess to help identify indiviudals that may have Ebola based on outside body temperature. This will eliminate a human from the process and reduce risk of contamination through bodily fluid. This will also increase the speed at which this project can be done. When deployed, it should end of being a system that isn't too expensive but can be utilized in many different environments. This specific piece of software will only be segmenting out the bright hot spots (like a head or a heat lamp). Later work will include possible temperature normalization, correcting for outside temperature, and possibly using IR to determine if an individual is sweating to normalize for that as well. 

I have not done any work on this project yet. There is a CS senior design team that originally started this project but I will not be using any of their work. There already exists a cython wrapper to get image data from the thermal camera. Something similar has been used at Hong Kong airports to find travels who have fevers from bird flu. There have been some studies as to the effectiveness of these kinds of systems, but many of the concerns seem to be related to how early of a stage the fever is as part of the illness [1]. This may be a valid concern as early stage Ebola symptoms begin between 2 and 21 days after exposure and only include a low fever, which may be much harder to detect from external body temperature. This will not be an issue for late stage Ebola which is often accompanied by a high fever Some studies have found that the head is the most optimal place to get a reading to corelate with core temperature [2]. Other studies ahve also found it to be less accurate for certain subsets of the population and only a weak correlation between outside and core temperature [3]. This will be different than previous work due to application because I will be inplementing it with two heat lamps as base temperatures for the thermal camera. Eventually this will also be integrated with a gating system to quarantine sick individuals. This could also be used for other illnesses besides Ebola but this particular application will be focused here.

I may use some OpenCV packages to track the location of the persons head if necessary. I want to make it as robust as I can without making it unnecessarily complex.



[1] International travels and fever screening during epidemics: a literature review on the effectiveness and potential use of non-contact infrared thermometers Bitar, D and Goubar, A and Desenclos, J C, Eurosurveillance, 14, 19115 (2009), https://doi.org/10.2807/ese.14.06.19115-en

[2] Chan, L. , Cheung, G. T., Lauder, I. J. and Kumana, C. R. (2004), Screening for Fever by Remote‐sensing Infrared Thermographic Camera. Journal of Travel Medicine, 11: 273-279. doi:10.2310/7060.2004.19102

[3] Detection of body temperature with infrared thermography: accuracy in detection of fever; Hong Kong Medical Journal, 2012, v. 18 n. 4, Suppl 3, p. 31-34
