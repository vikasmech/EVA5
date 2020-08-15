# Session 4

[collab link](https://colab.research.google.com/drive/1eEAji3GqmthwCTyOTMSEWBUXQmKrg4nJ?usp=sharing)

total number of parameters: 17,194

<img width="964" alt="Model Summary" src="https://github.com/vikasmech/EVA5/blob/master/S4/modelsummary.png">

Final Train log detail:
Train set: Average loss: 0.0025, Accuracy: 59971/60000 (99.95%)

final validation/test log detail:
Test set: Average loss: 0.0192, Accuracy: 9940/10000 (99.40%)

other additional things:
Batchnorm was used at after every convolution + relu layers (except last conv layer)
dropout of p= 0.1 was used twice. 
