# Music-Genre-Classification

## Introduction

This project implements and compares four deep learning classifiers trained on the GTZAN music dataset from Kaggle. The goal is to determine how well different neural network architectures perform in classifying music genres over 50 and 100 epochs. The classifiers include:

1.	Net1: Fully connected network
2.	Net2: Convolutional network (the architecture as the graph below)
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/cnn_architecture.png)
3.	Net3: Convolutional network with batch normalization
4.	Net4: Convolutional network with RMSProp optimizer

The networks were trained using Adam (for Net1, Net2, Net3) and RMSProp (for Net4) with a learning rate between 0.001 and 0.00001, adjusting according to the loss behavior. Training was conducted over 50 and 100 epochs for comparison.

## Results

### Net1
#### Confusion Matrix when epochs = 50 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net1_epoch_50.png)
#### Confusion Matrix when epochs = 100 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net1_epoch_100.png)

	•	Accuracy: 50.5% (50 epochs), 50.5% (100 epochs)
 -> Struggles to identify hip-hop and rock music, with no correct predictions for hip-hop (50 epochs) and only one correct prediction (100 epochs).
 
### Net2
#### Confusion Matrix when epochs = 50 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net2_epoch_50.png)
#### Confusion Matrix when epochs = 100 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net2_epoch_100.png)

	•	Accuracy: 62.38% (50 epochs), 66.34% (100 epochs)
-> Performs well in metal and reggae genres but struggles with rock classification.

### Net3
#### Confusion Matrix when epochs = 50 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net3_epoch_50.png)
#### Confusion Matrix when epochs = 100 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net3_epoch_100.png)

	•	Accuracy: 70.30% (50 epochs), 71.29% (100 epochs)
-> Highest accuracy among all models, but still weak in classifying rock music.

### Net4
#### Confusion Matrix when epochs = 50 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net4_epoch_50.png)
#### Confusion Matrix when epochs = 100 :
![image](https://github.com/mengchelee/Music-Genre-Classification/blob/main/net4_epoch_100.png)

	•	Accuracy: 65.35% (50 epochs), 62.38% (100 epochs)
-> Performs best with 50 epochs, showing strong predictions in classical, hip-hop, and metal genres.

## Conclusion

Net3 achieved the highest test accuracy, showing that batch normalization enhances model performance. However, all models exhibited poor performance in identifying rock music. Further improvements could include:

1.	Using a larger dataset.
2.	Applying advanced feature engineering.
3.	Exploring alternative architectures.
