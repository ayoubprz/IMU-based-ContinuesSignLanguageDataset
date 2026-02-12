# SignLanguage
This repository contains sign language numbers (gestures and movement).
There are two separate datasets here for isolated and continuous Persian Sign Language numbers. 

1. The first dataset, named ISLR, is for isolated numbers. This dataset consists of two files. 

    1.1 The first file contains numbers 0 to 9, which are expressed as static gestures without movement. The number of classes here is 10. 
  
    1.2 The second file includes numbers 10 to 9,000, expressed dynamically with movement.

     The number of classes here is 36:
       numbers 10 to 19 (10 classes),
       numbers 20, 30 to 90 (8 classes),
       numbers 100, 200 to 900 (9 classes),
       and numbers 1,000, 2,000 to 9,000 (9 classes).
    
The dataset was collected from 80 participants, each performing the corresponding sign once.

2. The second dataset, CSLR, is for multi-digit numbers (continuous recognition) and includes two-digit, three-digit, four-digit, and six-digit numbers. Complete information about this dataset is available in the readme file located in the respective folder.


These files are collected  with a glove equipped with 7 sensors (each has an accelerometer and a gyroscope)).
