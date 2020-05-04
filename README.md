# Baby-Crying-Detection-Based-on-Audio-and-Video-Fusion
# Introduction

 There are  dataset and code for paper which name is Research of Infant Crying Detection Method Based on Audio and Video Fusion. We create a public dataset about baby crying and  show some detail  code about how to finish our work about improve baby crying detection accuracy. We will introduce how to use this data and how to achieve crying sense by audio and video fusion  method in the following.





#  database 

We collect some data from AudioSet[1] project. It's aim to achieve a  standard data set in audio analysis. Firstly,we get youtube's URL and time interval from  AudioSet. It have 2300  data  sample  which not carefully handled. We deal those data and collect counter-sample data from UCF101[2]. finally,we get data distribution in the figure below.evey video sample paly  4s.evey aduio  also paly 4s and   correspond to the content of the video.

| catalogue     | baby crying | not baby crying | total |
| ------------- | ----------- | --------------- | ----- |
| audio dataset | 1200        | 1300            | 2500  |
| video dataset | 1200        | 1300            | 2500  |

you can download unprocessing data from  [here](https://drive.google.com/drive/folders/1DtA4jHovhmXTTyxqgjBVBKHSed9-whgT). We also  get these data from baiducloud:[baiducloud](https://pan.baidu.com/s/15TMa9GjYcWiUQJZDUQkB7A),extract code: sjpq.

  Download precessing  video data from [here](https://drive.google.com/drive/folders/1Bl-f6wEj_j5QbNH8t6aFX5EJ5cyYCIwe?usp=sharing).

 Download precessing  audio data from [here](https://drive.google.com/drive/folders/1Bl-f6wEj_j5QbNH8t6aFX5EJ5cyYCIwe?usp=sharing).

Some suggest  :  you can develop  self work by these dataset ,and you can put precessing audio and video data in our code at right file path.



#  How to run our code?

## tip:

We develop our code in google colab. so it just  publish a .ipynb file . And our paper  work have some fixed  in the finally push. We aim to prove dataset for your self work .And give you some suggest code if you want to use audio video fusion method .

 ## framework 

![image-20200504163153275](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200504163153275.png)

### 1 

 this path exit processing video data. The reason why  path  name is 3DCNN is that we create it do 3D conv example firstly.

## 2

SVM file path exit processing audio data . It is first use in SVM example . Both of 1 and 2 have two class : crying and no crying.

## 3 



# references



[1] Gemmeke J F, Ellis D P W, Freedman D, et al. Audio set: An ontology and human-labeled dataset for audio events[C]//2017 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). IEEE, 2017: 776-780.

[2]Khurram Soomro, Amir Roshan Zamir and Mubarak Shah, UCF101: A Dataset of 101 Human Action Classes From 

Videos in The Wild, CRCV-TR-12-01, November, 2012.