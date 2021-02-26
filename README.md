加入注意力机制的端到端语音识别，采用TIMIT数据集，对音频数据进行处理加工为MFCC特征，实现对音频音素的识别。  
Listener模块实现了三层pyramidal Bi-LSTM (pBLSTM)的结构对训练速度进行提升。  
![image](https://user-images.githubusercontent.com/78432083/109354819-55e0a280-78b9-11eb-9f17-ab5372653d17.png)  
![image](https://user-images.githubusercontent.com/78432083/109354882-6ee95380-78b9-11eb-92b1-f21315528f4d.png)  

Speller模块加入attention机制计算context vector改进传统循环神经网络。    
![image](https://user-images.githubusercontent.com/78432083/109354940-7f013300-78b9-11eb-9959-6a57e073d6e6.png)  
![image](https://user-images.githubusercontent.com/78432083/109354971-87596e00-78b9-11eb-9034-ab28d776b978.png)  
 ![image](https://user-images.githubusercontent.com/78432083/109354995-8e807c00-78b9-11eb-96cb-0b4fccec7a0d.png)  

Listener 和Speller的实现在model/las_model.py  
python3 train_timit.py <config file path> 进行训练
