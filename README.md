# Mulit-label Classification

## **Description** 
I built a mulit-label classification model that’s capable of detecting clothes and colors from image. Labels used for training are listed below:
* Black jeans
* Blue dress
* Blue jeans
* Blue shirt
* Red dress 
* Red shirt 

### **Sample output images** 
<p align="center">
  <img width="300" height="420" src="https://i.imgur.com/HzGTwGS.png">
  <img width="300" height="420" src="https://i.imgur.com/mlgmBoV.png">
</p>
 
LeNet5 was implemented in first version of this project, but after few tries and deep analysis I decided to use SmallerVBNet which turned out to have better resoults

Hiperparameters | Values
------------ | -------------
Batch size | 32 
Image resize | 96 
Image depth | 3 
Agumentation | Rotation range: 30 Width shift range: 0.1  Height shift range: 0.1 Zoom range: 0.2 Horizontal flip: True 
Optimizer | Adam 
Loss | Binary corssentropy 
Neural | network type SmallerVGNet 
Epochs | 50, 75, 150, 500, 1000 
 
 
### **Sample output plots*

#### **For 50 epochs**:  
![Dla 50 epoch](/models/epochs50.png)
 
Correctly recognized two labels: 68%  
Correctly recognized one label: 32%  
Not recognized any label: 0%  

#### **For 75 epochs**:  
![Dla 75 epoch](/models/epochs75.png)

Correctly recognized two labels: 74%  
Correctly recognized one label: 26%   
Not recognized any label: 0%  
 
#### **For 150 epochs**:   
![Dla 150 epoch](/models/epochs150.png)
 
Correctly recognized two labels: 71%  
Correctly recognized one label: 29%  
Not recognized any label: 0%  
 
#### **For 500 epochs**:
![Dla 500 epoch](/models/epochs500.png)
 
Correctly recognized two labels: 77%  
Correctly recognized one label: 23%  
Not recognized any label: 0%  
 
#### **For 1000 epochs**: 
![Dla 1000 epoch](/models/epochs1000.png)
 
Correctly recognized two labels: 74%  
Correctly recognized one label: 26%  
Not recognized any label: 0%
