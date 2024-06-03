# Machine learning codes for "Data-driven discovery of self-similarity using neural networks"

## Contents
There are three ipynb files and two numerical data text files.
Analysis within the paper can be simulated by running these files.
The content of each file is as follows.




## Neural network analysis for the viscoelastic board experiment
The ipynb files, "one_variable_search_synthetic.ipynb" and "one_variable_search_experiment.ipynb", deal with the viscoelastic board experiment.
We have confirmed that these codes work with Python 3.10 and matplotlib 3.7, and also with Python 3.12 and matplotlib 3.9.
"one_variable_search_synthetic.ipynb" is for synthetic analysis, that is, generating synthetic data and training the neural network using it.
The file consists of definitions of neural networks and functions necessary for training, followed by sections that actually output the results of their execution.
These can be run in order from the top to simulate the results described in the paper.
The strength of the noise added to the synthetic data can be adjusted when generating it.
Fluctuations in the training results due to these noises can also be estimated by performing a bootstrap analysis as described in the code.

"one_variable_search_experiment.ipynb" is for training with actual experimental data.
By entering the path of the data in the appropriate part of the code and executing the code from the top, training can be performed on the experimental data.
Since experimental data contains fewer data points than synthetic data, and also contains errors, there is some variation in the training results. 
The experimental data are stored in Data_ExperimentDynVisSurf.txt.
The details of the experimental data are explained in the separate file "Readme for Data_ExperimentDynVisSurf.ipynb".




## Neural network analysis for more general cases
The ipynb file "two_variable_search.ipynb" deals with more general cases where the scaling functions have two arguments.
There are two examples in the file, the first one being a virtual system and the second one being the Zener viscoelastic model.
For the Zener viscoelastic model, the training is performed using two types of synthetic data, depending on whether or not the constraints of the actual experimental environment are taken into account.
Since the scaling functions have two arguments, the graph of training results from a neural network becomes a two-dimensional surface.

We have confirmed that these codes work with Python 3.9 and matplotlib 3.7.