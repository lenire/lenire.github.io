---
layout: post
title:  "Can't stop the signal"
date:   2020-03-22 00:01:46 -0500
categories: RaspberryPi, Arduino
---
Today was two big projects for me.  Build a Light Theremin with my Arduino and turn my Raspberry PI into a pirate radio station.</p>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OJ99SFnLbqA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

    I followed the tutorial in my book, and was able to create it in no time. It is really annoying, but it was neat to see how the photo sensor works. The next tutorial turns it into a keyboard, but I wonder if you can combine the two inputs as they make a more interesting sound.

    The other big project I worked on today, was to turn my Raspberry PI into a pirate radio station. 

    I used the following commands to get my Raspberry PI setup

    pi@raspberrypi:~/PiFmRds/src $ history
      sudeo apt-get update
      sudo apt-get upgrade
      sudo apt-get install libsox-fmt-mp3 
      sudo apt-get install libsndfile1-dev 
      sudo apt-get install git 
      git clone https://github.com/ChristopheJacquet/PiFmRds.git 
      cd PiFmRds/src 
      make clean 
      make
 
    The following command then turned on the transmitter to get the Raspberry PI to start broadcasting: 
      sudo ./pi_fm_rds

     I do not actually have a radio setup in my home, so the Pirate Station was short lived.

 But I will be uploading it again, and then running my music through it.