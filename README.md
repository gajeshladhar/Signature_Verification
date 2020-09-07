# Signature Verification

A Deep Learning Model in Keras Format, which takes input two Images and return 1 if that signature are done by same person, otherwise 0.
We used siamese Network Architecture for this.
<br>
This is explaination of entire Project :
<br><hr></hr>
<img src="https://i.ibb.co/85B3X3p/Screenshot-from-2020-09-07-20-58-30.png">
<font color="blue"><br><br><hr></hr><br><br><b>Download The DataSet from CEDAR and BHSig-260, we have saved this in drive, here is a code for loading dataset</b></font>
<br><br>
<img src="https://i.ibb.co/LQr6dhs/Screenshot-from-2020-09-07-21-06-11.png"><br>
<br><hr></hr><br><br>
<b> We have Pre-Processed raw Data, here are some steps :</b><br><br>
  1). Convert Images to Binary Images<br>2). Apply some filters to resize edges of signatures.<br>3). Invert Values in Binary Images.<br>4).Rotate some Images than add those new Images.<br>5). Use the shering and Add new images.<br>6). Normalize all Images
<br><br><hr></hr><br><br>
<b> We used Contrastive Loss Function in Training </b><br><br>
<img src="https://i.ibb.co/cv4WXB7/Screenshot-from-2020-09-07-21-14-51.png"><br><br>
<hr></hr><br><br>
<b> Model Architecture : </b><br>
<img src="https://i.ibb.co/gZMg2vL/model.png">
<br><br><hr></hr><br><br>
<b> Model at Test Time : </b><br>
In Test time we will give input of two signature images one of them is original and other is testing image,<br>
If, our last Lambda layer which is nothing but a distance vector returns distance which is Less than some thresold then, we will consider both signature to be done by same person otherwise there is some forgery in both signatures.

