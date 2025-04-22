#Phase II Update!

At this stage, we are happy to report that the DS-CNN model has been trained and integrated with the maze game code. The game is running with laptop onboard mics and is functional. The only caveat is the implementation of the 
game on the PYNQ-Z1 board; there have been numerous challenges, but we are confident that with the strides we have made thus far, it will be working by delivery date.

##DS-CNN Update:
- model has been implemented!
- model has been trained on the dataset
- resulting .tflite file was put on the FPGA (as a lightweight, trained model which can run inference)
See speechCommand.ipynb!


##Game Update:
- found public domain game
-> found out that pygame will not run on jupyter notebook
- built our own game that employs available graphing tools to mimic a maze design


##Integration Update:
- found out that the version of python installed on the pynq board was not directly compatible with tflite-runtime
-> installed Python 3.7 on FPGA
- installed tflite-runtime in a new environment on the FPGA which ran on the new python version
- installed all necessary pacakges related to jupyter notebook, numpy, etc in new environment
#now, tflite-runtime is operational on a new kernel designed for our project. still in process is the installation of pynq overlays to be able to use the onboard mic
- we investigated using sounddevices as a possibility for audio collection, but the audio libraries associated with it could not detect the board's microphone
- some of the difficulty in installing pynq overlays on the board is integrating the files related to the hardware with the new kernel environment, but we expect it to be working soon
