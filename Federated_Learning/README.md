# Federated Learning on Semantic Segmentation task (FedAVG, FedADMM)
Federated Learning is one the new eras of Deep Learning which aim is to train a global Network with respect to provate local netwroks. Leaning on smart phones and medical tasks are some of important applications of Federated learning.

In this Project, I've used federated learning for Image segmentation of Autonomous Driving cars data. We can consider network of each car as an private and local network and we want to tran a global network to be robust against perturbations.
This project is a Pytorch Implementation of two papers 
- "FEDERATED OPTIMIZATION IN HETEROGENEOUS NETWORKS" by  Tian Li et al which introduces the FedADMM algorithm for aggregation of weigths of local networks
- "Communication-Efficient Learning of Deep Networks from Decentralized Data" by H. Brendan McMahan et al which introduces the Federate learning for the first time and uses the average aggregation method.

## Data
I've devided Camvid Dataset which is a famous dataset for segmentation, for each local network and local networks datasets are Non-IID.  


## Model
For segmentation task, I've used SegNet. we have multiple local SegNet Networks for each Autonomous car and a Global Network for Aggregating weights of local networks. All of the Networks have same Architechture.

Below Loss function of Both Aggeregation methods are shown:  
  
- Loss function of Average Aggregation during communication rounds for 3 local networks and one global network  
  
![average loss](loss_primal_3local.jpg "average loss")
  
- Loss function of ADMM Aggregation (FedADMM) during communication rounds for 2 local networks and one global network  
  
![admm loss](loss_admm_2local.jpg "admm loss")

## Results
  
Some of segmented images with the fedADMM aggregation is in blew figure, we can see that this method works as well as [centralized training of segnet](https://github.com/amirhosein-mesbah/Deep_Learning/tree/main/Image_Segmentation_SegNet)  
   
![output admm](output_admm.jpg "output admm")

