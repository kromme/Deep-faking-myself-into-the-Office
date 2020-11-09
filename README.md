# Deep-faking-myself-into-the-Office
Using DeepFakeLab to change Michael Scott's face with mine

In the last couple of years, my Data Science interest went mostly towards text (NLP / NLU), but that does not prevent me from playing around with other types of data, like video. Inspired by Trump’s response to his Corona approach and Jim Carrey vs Allison Brie, see my first attempt at playing with DeepLearning for video and DeepFakes.  

Check the video at: https://medium.com/@j.kromme/deepfaking-myself-in-the-office-a5585549acb5

This repo shows what I have done, I do not claim to have any rights of the video or to the code.

![](https://miro.medium.com/max/700/1*iJJjeYl0m3P81oHGzxvJTQ.png)

## Preperations
1. Clone the repo at https://github.com/iperov/DeepFaceLab.  
2. Find a video where you want to put a / your face on. I choose: https://youtu.be/OkN6OV-ueTQ.  
3. Create a video of around 20 minutes of yourself. I just recorded myself while I was working. I actually found the clip from The Office while I was recording, looking back, I would definitely first find the video. The reason is quite simple, if you imitate the destination video, the results will be better.  
4. Some tips:  
* Try to get the lighting the same: mine was too light.  
* Imitate speech: as i was filming while working, I didn’t really speak, so in the results my teeth are somewhat blurry and “Jeroen Scott” doesn’t articulate that well.  
* Maybe I should have shaved.  

## DeepFake Steps
1. clear workspace.bat  
2. extract images from video data_src  
3. extract images from video data_dst FULL FPS.bat  
4. data_src faceset extract.bat  
5. data_dst faceset extract.bat  
6. train SAEHD.bat. I used the SAEHD for training, there are other options, but from all the blogs I read, this one was use most.  
7. TIP: go away for the weekend. The fans of your computer will have a hard time cooling it and thus produce quite some noise. You won’t be able to concentrate on other stuff without earplugs. Or simply use the cloud!  
My main question here was: how long do I need to train, and I found multiple answers. One said three to seven days (wow big help), another said until you reach a loss of 0.02. Well I got to 0.16 after four days, the next day I needed to go work again and didn’t want to be distracted by the noise of my computer so I stopped. (You can always pick up the training at a later stage!) and I am quite happy with the results.  
8. merge SAEHD.bat  
9. merged to mp4.bat. There is an interactive shell which allows you to alter things like the size of your head (I didn’t need to change), skin color (ended up using mix-m) and other stuff. The secret here: almost nobody knows what is really happening here, just try some stuff out  
