# Smart Christmas Tree:

A Christmas tree with addressable LEDs that can perform light shows, syncing to festive music. 

## Inspiration

My "Smart Tree" was my last and Christmas themed passion project of 2025. 
For years I've been enchanted by festive houses (on the particular show, Christmas Light-Fight) decked-out in Christmas lights that blink and dance to the rhythm of holiday music. 
I've always yearned to flaunt my holiday spirit in a similar way; with an extravagant light show that I can control. 
Last November, I stumbled upon a video of a tree decked out in addressable LEDs, however unlike other lightshows, the colors traveled up, down, left, and right across the tree-- they weren't bound to the string of lights. 
The concept was finding and mapping the positions of the lights onto a spatial coordiate grid. 
I was thoroughly inspired to make my own, and formulated a plan to emulate the same capabilites of the tree in the video.

## Project Goals

Some Goals I had for the project:
- achieve a tree with lights which can be controlled by their spatial 2d coordinates (x,y) 
- sync the lights to a few songs to create my own 'light shows'
- learn the hardware components (addressable lights), how they recieve power, etc.
- integrate my vision software into the hardware of the lights
  
## 'Smart' Solution

- use a webcam/OpenCV to capture each individual LED on the tree as it lights up (going from the string)
- send these frames to a python file, which then uses openCV to find the contours in the LED and darker background, estimates the position(s) of the contours
- takes the average of all the coordinate points to find center of LEDs and writes it into a text file
- my c code reads out of the text file, sorts the x's and y's in asc/desc and saves them into a makeshift hashmap (😂 dictionary )
- from c file, control the lights by their positions on the hashmap 

## Tech Stack

### Hardware
- Raspberry Pi
- WS2811 Addressable LEDs
- USB Webcam
- 12V 10A Power Supply
### Software / Tools
- Python
- C
- OpenCV
- Raspberry Pi OS
- VNC Viewer (for easier development)
  
### References
- link repo ws2811 here


## Features

## Hardware / Supplies

## Setup
