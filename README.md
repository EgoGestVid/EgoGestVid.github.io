## **EgoGestVid**
Synthetic Video Generation Framework for Robust Hand Gesture Recognition in Augmented Reality Applications

# Abstract
Hand gestures are a natural means of interaction in Augmented Reality and Virtual Reality (AR/VR) applications. Recently, there has been an increased focus on removing the dependence of accurate hand gesture recognition on complex sensor setup found in expensive proprietary devices such as the Microsoft HoloLens, Daqri and Meta Glasses. Most such solutions either rely on multi-modal sensor data or deep neural networks that can benefit greatly from abundance of labelled data. Datasets are an integral part of any deep learning based research. They have been the principal reason for the substantial progress in this field, both, in terms of providing enough data for the training of these models, and, for benchmarking competing algorithms. However, it is becoming increasingly difficult to generate enough labelled data for complex tasks such as hand gesture recognition.

# Idea

![](https://github.com/EgoGestVid/EgoGestVid.github.io/blob/master/imgs/framework.png)
![no-alignment]({{ '/imgs/framework.png' | absolute_url }})

In this work, we propose a neural network architecture that is capable of generating a sequence of video frames given an input mask layout. These masks passed in succession to the generator network results in a video sequence with given background image. We can even use different video frames as input (passed successively) for the background. This results in videos with both static and dynamic backgrounds.

# Framework

![](https://github.com/EgoGestVid/EgoGestVid.github.io/blob/master/imgs/outline.png)
![no-alignment]({{ '/imgs/outline.png' | absolute_url }})

We used the ability of the model outlined by Turkogluet al. to generate video sequences with different backgrounds but same (or controlled) fingertip and hand as in the reference input image. The proposed framework sequentially composes a scene, breaking down the underlying problem into foreground and background separately. Our approach utilises the foreground generator as proposed by Turkoglu et al. to superimpose elements over the given background.  Such a network allows us to control various properties, including fingertip location, as well as hand’s shape and appearance.

# Results

- **Using CycleGAN**<br>
![no-alignment]({{ '/imgs/fig_inputoutput-1.jpg' | absolute_url }})

- **Synthesised using our approach.**<br>
<p align="center">
  <img height="50%" width="50%" src="/imgs/domain_shift-1.jpg">
</p>

<br>Clearly, images are more clearer and the segmentation masks give us control over the fingertip location, hand's appearance, shape, size and so on.

# Gestures

Our approach gives us the capability to generate a very large synthetic egocentric gesture pointing dataset. A few examples are shown below:

- **A circle pointing gesture** <br>
<p align="center">
  <img height="50%" width="50%" src="/imgs/circle-1.jpg">
</p>
  
-  **A square pointing gesture** <br>
<p align="center">
  <img height="50%" width="50%" src="/imgs/square.png">
</p>
  
# Video

<a href="https://youtu.be/M5ADsP4l9Zo" target="_blank"><img height="50%" width="50%" src="/imgs/video.png" border="50" /></a>







