Name: Makenzie Brian
Class: ME 599
File: Project Proposal

This project is intended to be a deep learning layer calculator. This will be used in the auto-encoding state representations from raw lidar data for multi-agent reinforcement learners project. The user will specify, at a minimum, the input and output data dimensions they wish to have upon completion, as well as the desired layer architecture. The program will then calculate the dimensions of the intermediary layers (possibly with a semi-brute force search), create and save a PyTorch model of the neural network. This is helpful for those who have some experience in deep learning but not enough to intuitively know how to configure the layers. This is difficult because each layer reduces the dimensionality of the data going through it as a function of filter size and stride. I plan for this program save a file of the neural network model so it can then be used by the application. Additional work may include a visualization of the neural network architecture upon completion, but this may prove to be outside the scope of what is reasonable.

I have not done any work on this project yet. The equations for this project are mostly some simple algebra and are already known but not implemented in Python and currently has to be entered separately from the implementation and does not yield any visualization. 

I will be using PyTorch for some of the modeling implementation [1]. I may also use additional packages based on PyTorch for the visualization portion of this implementation because PyTorch does not appear to have a good visualization tool built into it [2].

[1] “Tensors and Dynamic Neural Networks in Python with Strong GPU Acceleration.” Reinforcement Learning (DQN) Tutorial - PyTorch Tutorials 0.4.0 Documentation, pytorch.org/.

[2] Utkuozbulak. “Utkuozbulak/Pytorch-Cnn-Visualizations.” Pytorch Implementation of Convolutional Neural Network Visualization Techniques, GitHub, github.com/utkuozbulak/pytorch-cnn-visualizations.
