# Posisi Direktori

**Detection**
|--->Detection.py
|--->SDN.py
|--->switch.py
**generate_ddos_traffic**
|--->**__pycache__**
      |--->collect_ddos_traffic.cpython-39.pyc
      |--->switch.cpython-39.pyc
|--->collect_ddos_traffic.py
|--->generate_ddos_traffic.py
|--->switch.py
**generate_normal_traffic**
|--->collect_normal_traffic.py
|--->generate_normal_traffic.py
|--->switch.py
**Major Project Documentation.pdf**
**README.MD**
**instructions.txt**

Posisi direktori diatas untuk membantu kita memahami posisi file ketika ingin menjalankan simulasi SDN.
_Generating Normal traffic:
run command ryu-manager collect_normal_traffic.py in generate_normal_traffic folder.
run command "service openvswitch-switch start"
run command sudo python generate_normal_traffic.py in generate_normal_traffic folder.
Restart PC:
Generating DDoS traffic:
run command ryu-manager collect_ddos_traffic.py in generate_ddos_traffic folder.
run command "service openvswitch-switch start"
run command sudo python generate_normal_traffic.py in generate_ddos_traffic folder.
Restart PC:

Detecting Attacks and Normal Traffic:
run command service openvswitch-switch start
run command ryu-manager Detection.py in mininet folder. 
run command sudo python SDN.py in mininet folder
after the above command in the same terminal, run command xterm h1 h6 h13 h17.

Normal traffic
ping 10.0.0.15 on node h17 then ping 10.0.0.4 on h6
go to h13 do cd .. ls, clear, git clone, wget etc commands
stop
DDOS traffic:
hping3 is a network tool to perform ddos attacks.
now on node h17 ping 10.0.0.18
on node h6 hping3 -1 -V -d 120 -w 64 -p 80 --rand-source --flood 10.0.0.12 icmp flood
hping3 -S -V -d 120 -w 64 -p 80 --rand-source --flood 10.0.0.12 syn flood
hping3 -2 -V -d 120 -w 64 -p 80 --rand-source --flood 10.0.0.12 udp flood
hping3 -1 -V -d 120 -w 64 -p 80 --rand-source --flood -a 10.0.0.12 10.0.0.12 smurfs_






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
