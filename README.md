# Posisi Direktori
![Screenshot 2024-05-22 114944](https://github.com/201solafide/Reproduce_Code/assets/146401936/e35abcde-64c4-4ca9-8ac5-6b91dd7c022e)
![Screenshot 2024-05-22 115431](https://github.com/201solafide/Reproduce_Code/assets/146401936/ee38a8e4-d609-43ff-be57-bf7351f00253)
![Screenshot 2024-05-22 115546](https://github.com/201solafide/Reproduce_Code/assets/146401936/9efeaf01-675a-4327-8760-cd904d52d040)
![Screenshot 2024-05-22 115555](https://github.com/201solafide/Reproduce_Code/assets/146401936/94620247-e0f9-4353-baee-0d1f136dcf29)
![Screenshot 2024-05-22 115603](https://github.com/201solafide/Reproduce_Code/assets/146401936/d6500665-6d75-41bd-9536-1bfbccb137e1)
![Screenshot 2024-05-22 115609](https://github.com/201solafide/Reproduce_Code/assets/146401936/ba2ec292-8238-45a3-9170-2decc55e5dc8)

# Detection-of-DDoS-attacks-on-SDN-network-using-Machine-Learning-
* Designed and deployed local SDN network using mininet. Tools such as hping3 , iperf are used to generate DDoS
and Normal traffic.
* Designed and developed various Machine Learning models using RapidMiner to perform comparitive analysis on
accuracy of various Machine Learning models using this locally generated dataset.
* Best performing model among them was selected and deployed on the SDN network to monitor and detect DDoS
network traffic.
* This application requires high compute resources, make sure you have decent VM or PC.
Simulation of SDN  network and generating our own dataset using iperf and hping3 tools. This locally generated dataset is used to train various models and compare their performance. The best performing model is chosen to be deployed on network to monitor traffic and detect DDoS attacks and alert which host is the victim.
I have used RapidMiner tool to rapidly build , train , test and evaluate the performance of of K-NN,SVM,RF and DL. RF has the overall best accuracy. Therefore it is chosen to monitor and detect attacks on our sdn network. 
Read PDF for more information.
SDN network Topology  

![Screenshot_20230224_064538](https://user-images.githubusercontent.com/49368483/221187802-1eb88280-0df1-49ad-8a74-c52daa939202.png)

Detecting Normal Traffic

![Screenshot_20230224_064617](https://user-images.githubusercontent.com/49368483/221187833-81e98571-bd85-4b80-9ec7-a103e6f0c349.png)

Detecting DDoS Traffic

![Screenshot_20230224_064633](https://user-images.githubusercontent.com/49368483/221187857-c1599400-2cef-4304-9e2c-6cc246d877eb.png)
