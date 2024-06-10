# TITLE 
Emma BOTHEREAU∗ , Alice CHILLET∗ , Robin GERZAGUET∗ , Matthieu GAUTIER∗ , Olivier BERDER∗ , 
∗ Univ Rennes, CNRS, IRISA, firstname.name@irisa.fr



In this repository are presented the Neural Networks used for the article in Julia. 

## Description

We used the following neural networks :
- [POWDER CNN](https://ieeexplore.ieee.org/document/9348261)
![](Illustrations/POWDER.png)
- [Sankhe CNN](https://ieeexplore.ieee.org/document/8882379)
![](Illustrations/Sankhe.png)
- [Elmaghbub CNN](https://arxiv.org/abs/2308.04467) 
![](Illustrations/Elmaghbub2.png)
- [WiSig CNN](https://arxiv.org/abs/2112.15363)
![](Illustrations/wisig.png)
- [Feng CNN-GRU](https://ieeexplore.ieee.org/document/9851177) 
![](Illustrations/Feng.png)
- Triple Dense
![](Illustrations/TripleDense.png)

## Learning rates for each Network-Dataset combination

All networks undergo 200 epochs of training on the S1 scenario only, with early stopping if the loss function (CrossEntropy) does not decrease for 10 consecutive epochs. We used the Adam Optimizer with the corresponding learning rate. Per default, we used a scheduler, reducing by 10% the learning rate, every 10 epochs.

|                     | **POWDER CNN** | **Sankhe CNN** | **Elmaghbub CNN**  | **WiSig CNN** | **Feng CNN-GRU** | **Triple Dense** |
|---------------------|----------------|----------------|-------------------|---------------|------------------|-------------------------|
| **POWDER Dataset**   | 0.0001         | 0.0001         | 0.0001           | 0.0001        | 0.0005*           | 0.01                  |
| **Wisig Dataset**  | 0.0001         | 0.00001         | 0.0001                  | 0.0001        | 0.0001           | 0.01                    |
| **Elmaghbub Dataset**| 0.0001         | 0.0001         | 0.0001               | 0.001        | 0.005*          | 0.01                  |
| **Oracle Dataset**  | 0.0001       | 0.0001         | 0.0001           | 0.001        | 0.001           | 0.01                  |


*The scheduler reduce by 10% the learning rate, every 30 epochs, early stopping if loss did not reduced for 30 epochs
