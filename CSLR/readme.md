Continuous Sign Language Recognition Dataset (Inertial Sensor-Based)

*** Project Description ***

  This dataset has been developed for continuous sign language word recognition using inertial sensor data.
  The recorded gestures correspond to multi-digit numbers, as these can be expressed using movements of a single hand only. 
  Head movements and other body parts do not influence the gestures, ensuring that the dataset focuses exclusively on hand motion dynamics.
  The primary goal of this dataset is to facilitate research on continuous sign language recognition using wearable inertial sensing devices.

*** Sensor Configuration ***

  Data were collected using a custom-designed glove equipped with the following inertial modules:
  
      1 × MPU9250 (9-axis IMU)
      
      6 × GY-521 modules, each containing:

        1 accelerometer
        
        1 gyroscope

*** Sensor Placement ***
          
  The MPU9250 module was placed on the back of the hand.
  Five GY-521 modules were placed on the fingertips.
  One GY-521 module was placed on the wrist.
  * Due to the high similarity between the motion data recorded from the back-of-hand module and the wrist module during number gestures, the wrist sensor data were excluded from the final dataset.
  Therefore, the final dataset contains data from six active sensor modules.

*** Sampling Rate ***

  The data were recorded at a sampling frequency of:  60 Hz

*** Participants ***

  The dataset was collected from 41 participants aged between 15 and 32 years.
  27 individuals (8 women and 19 men) were deaf or hard-of-hearing and fully proficient in sign language gestures.
  The remaining participants (5 women and 9 men) were students familiar well with the required gestures.

*** Recording Protocol ***

  Each participant performed gestures corresponding to multi-digit numbers once, and the resulting data were recorded.
  The dataset captures continuous motion sequences, including transitional movements between digits.

*** Data Format ***

  The dataset is organized into separate files for:
      Two-digit numbers
      Three-digit numbers
      Four-digit numbers
      Six-digit numbers
  Each file is stored in NumPy (.npy) format and has four dimensions:
      (samples, time_frames, modules, features)
  Dimension Description
    First dimension (samples) represents different recorded gesture sequences.
    Second dimension (time_frames) is the number of temporal frames for each sample.
    Third dimension (modules) represents the 6 active sensor modules.
    Fourth dimension (features per module), Each module contains 6 values:
        First 3 values: Accelerometer data (x, y, z)
        Next 3 values: Gyroscope data (x, y, z)

*** Label Structure ***

  Labels for the two-, three-, four-, and six-digit datasets are stored separately in NumPy (.npy) files.

*** Frame-Level Annotations ***

  For the two-, three-, and four-digit datasets, and for 43 samples of the six-digit dataset, the starting and ending frame indices of each digit are provided.
  For each digit:
      The first number represents the start frame of the gesture.
      The second number represents the end frame of the gesture.
      The frames between the end of one digit and the start of the next digit correspond to transitional hand movements.

*** Example: Loading the Dataset ***

  The dataset can be easily loaded using NumPy:
      import numpy as np
      d2 = np.load("./twoDigitsContDataset.npy")
  The above command loads the two-digit continuous dataset, which contains 504 samples.

*** Intended Use ***

  This dataset is intended for:
      Continuous sign language recognition
      Sequence modeling (LSTM, BiLSTM, GRU, Transformer, etc.)
      Sensor-based gesture recognition
      CTC-based temporal segmentation
      Human motion analysis using IMU signal
