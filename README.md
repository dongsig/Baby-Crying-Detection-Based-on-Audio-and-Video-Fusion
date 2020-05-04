# Baby-Crying-Detection-Based-on-Audio-and-Video-Fusion



[TOC]



# Introduction

 There are  dataset and code for paper which name is Research of Infant Crying Detection Method Based on Audio and Video Fusion. We create a public dataset about baby crying and  show some detail  code about how to finish our work about improve baby crying detection accuracy. It will introduce how to use this data and how to achieve crying sense by audio and video fusion  method in the following.





#  database 

We collect some data from AudioSet[1] project. It's aim to achieve a  standard data set in audio analysis. Firstly,we get youtube's URL and time interval from  AudioSet. It have 2300  data  sample  which not carefully handled. Next, deal those data and collect counter-sample data from UCF101[2]. finally,we get data distribution in the figure below. every video sample play  4s. every audio  also play 4s and  correspond to the content of the video.

| class         | baby crying | not baby crying | total |
| ------------- | ----------- | --------------- | ----- |
| audio dataset | 1200        | 1300            | 2500  |
| video dataset | 1200        | 1300            | 2500  |

you can download not processing data from  [here](https://drive.google.com/drive/folders/1DtA4jHovhmXTTyxqgjBVBKHSed9-whgT). We also  put these data into baiducloud:[baiducloud](https://pan.baidu.com/s/15TMa9GjYcWiUQJZDUQkB7A),extract code: sjpq.

  Download precessing  video data from [here](https://drive.google.com/drive/folders/1Bl-f6wEj_j5QbNH8t6aFX5EJ5cyYCIwe?usp=sharing).

 Download precessing  audio data from [here](https://drive.google.com/drive/folders/1Bl-f6wEj_j5QbNH8t6aFX5EJ5cyYCIwe?usp=sharing).

Some suggest  :  you can develop  self work by these raw dataset  or put precessing audio and video data in our code at right file path to run.



#  How to run our code?

## tip:

We develop our code in google colab. so it just  publish a .ipynb file . And our paper  work have some fixed  in the finally push. It aim to prove dataset for your self work .And give you some suggest code if you want to use audio video fusion method .

 ## framework 

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504173936373.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xpdXBlbmcxOTk3MDExOQ==,size_16,color_FFFFFF,t_70)

###  1 

 this path exist processing video data. The reason why  path  name is 3DCNN is that we create it do 3D conv example firstly.

###  2

SVM file path exist processing audio data . It is first use in SVM example . Both of 1 and 2 have two class : crying and no crying.

###  3 

 We deal our data  use ffmpeg  library . however,I have remove those process code into finishwork.ipynb. So ,this file just is processing demo  without any use.

###  4 

  This text file exist all message about baby crying dataset,you can download 2300 video from a.text .It has youtube ID 、crying start time、 crying end time.  We hope this file help for you looking forward origin.

###  5 

It is key file  in our work. I put almost all work in this file .But  It is not finally version in our paper.  The final version of the work need contact qq:2425497621 duce some  cooperation with hospital.

##  Step ( run finshwork.ipynb in colab)



**step 1: deal data ** 

At first,we use  4 unit  code  deal  raw  data .It generate  3DCNN and SVM path.

**step 2: extract  input data** 

 We extract some feature and input from 3DCNN and SVM. And save them.

**step 3:  train SVM** 

 Train data by SVM  method.

**step 4:  train CNN** 

 Train data by CNN method.

**step 4:  train 3DCNN ** 

 Train data by 3DCNN method. In this unit we solve the problem of timing synchronization  at first. the detail please read 

function read_data().



**step 5:  train LSTM** 

 Train data by LSTM method.

**step 6:  train audio and video fushion menthod ** 

 Train data by audio and video fushion menthod . There have four  method achieve by keras framework . We suggest you use tensorflow.keras .It also support TPU. 



##   Result

The result of our finally work.

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020050417400116.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xpdXBlbmcxOTk3MDExOQ==,size_16,color_FFFFFF,t_70)



# [references](https://blog.csdn.net/liupeng19970119/article/details/105920607)



[1] Gemmeke J F, Ellis D P W, Freedman D, et al. Audio set: An ontology and human-labeled dataset for audio events[C]//2017 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). IEEE, 2017: 776-780.

[2]Khurram Soomro, Amir Roshan Zamir and Mubarak Shah, UCF101: A Dataset of 101 Human Action Classes From 

Videos in The Wild, CRCV-TR-12-01, November, 2012.



#  Supplementary explanation

if readme.md file is't work ,please open my blog  at [here](https://blog.csdn.net/liupeng19970119/article/details/105920607)