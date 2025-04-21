# Project_Template

## FPGA Project Group 4

## Team Members:
- Lisa Berlizova
- Troy Harmon
- Tessa Heick

## Project Title:
### a-MAZE-ing Marvin: A voice activated maze game run on a PYNQ-Z1 board via TinyML network.


## Project Description and Motivation:
Online games have become an essential aspect of modern entertainment, offering experiences that
range from expansive multiplayer worlds to minesweeper on Google Chrome. However, many games rely
on the physical dexterity of players, requiring consoles, keyboards, or motion detection systems. This can
be challenging for individuals with limited mobility or finger strength. Thus, voice-controlled movement
in tandem with a single button system can provide an alternative, making simpler games more accessible
to a wider audience.
This project looks to integrate an existing maze game built with the Pygame library with a
keyword detection system to create an accessible game run on an FPGA board (the PYNQ-Z1 to be exact). It
will use the onboard microphone and button peripherals to capture audio from the player, which is then used
by the DS-CNN (depthwise separable convolutional neural network) to identify keywords, which will act as directions to move the player’s character through the maze. The FPGA will be running a Jupyter Notebook via ethernet to display the game on a nearby
monitor.

## Context: DS-CNN
FPGAs are often used for acceleration, and convolution operations lend themselves well to acceleration. Two approaches are employed in this project, one in software and one in hardware. In software, a depthwise separable convolutional neural network (DS-CNN) is employed. Instead of performing regular convolution on the input, DS-CNN splits the multidimensional kernel into smaller parts, drastically cutting down on the number of multiplications needed to achieve the same result. In hardware, a custom overlay will be explored to further accelerate the convolutions. 
The employment of FPGAs in keyword detection is not a novel concept; a variety of networks have been deployed on FPGAs to achieve reliable, local detection. While the recognizable words are limited to a smaller subset of the English language, the security of voice data is ensured and latency is improved through utilization of local hardware. Other voice-controlled games, such as chess have successfully been implemented on FPGAs, and the feasibility of running a DS-CNN on embedded systems has been well established. These proven concepts will be integrated with an established, public-domain maze game by removing the original movement controls from the game, and replacing it with the outputs of the neural network.

## Key Objectives:
- Implement a DS-CNN that is capable of identifying keywords used in a maze game, such as "up", "down", etc.
- Configure the FPGA to collect user audio and efficiently process the data to a format usable by the DS-CNN model.
- Launch the algorithm on the PYNQ-Z1 board while establishing interfaces for audio from the onboard microphone other user inputs from the physical board to the Jupyter Notebook through the ethernet connection.
- Integrate a publicly available maze game with the keyword detection system replacing standard keyboard inputs.

## Technology Stack:
- PYNQ-Z1 board
- Ethernet cable
- PC/Laptop
- Monitor
- Jupyter Notebook (Python)
- Maze game from Pygame Repository: [PyMaze](https://www.pygame.org/project/733)
- Vivado
- Keyword Audio Dataset: #Link?
- External microphone (if onboard microphone is not sufficient for clean audio capture)

## Expected Outcomes and Deliverables:
- Create and demonstrate a locally run, voice-controlled maze game.
- Generate a detailed description of the design process to be used for recreation and documentation of project.
- Create presentation showing major milestones of design process as well as intermediate and final results.
- Figures, text, and code snips explaining major processes behind word recognition, use of FPGA hardware, and game control.

## Tasks:
- [ ] Lisa: Create and share Jupyter Notebook with necessary libraries for DS-CNN
- [ ] Lisa: Load keyword dataset into the notebook and train a DS-CNN model for keyword recognition
- [ ] Tessa: Configure FPGA board to collect audio data using onboard microphone
- [ ] Tessa: Establish interface between FPGA button/microphone peripherals and the Jupyter Notebook to allow the Python program to process audio and classify keywords
- [ ] Tessa/Troy: Develop any overlays or audio processing needed before microphone audio can be passed to the DS-CNN
- [ ] Lisa: Test DS-CNN accuracy and speed using audio of keywords captured with FPGA board
- [x] Troy: Find open-source, simple maze game that can be modified and run in Python
- [x] Troy: Transfer game code to Jupyter Notebook and make any modifications needed for the game to run and display properly
- [x] Troy: Develop interface for the user to play the game using outputs from the DS-CNN rather than keyboard inputs.
- [ ] All: Document progress and highlight significant challenges/obstacles
- [ ] All: Perform full testing of the game and add easter eggs or additional features

## Timeline:
(Provide a timeline or milestones for the project)
- April 4th - April 18th: Get game working
- April 5th - April 8th: Create Jupyter Notebook, transfer game to notebook, and generate initial DS-CNN model.
- April 9th - April 14th: Create interface for audio data collection and processing. Perform initial testing of DS-CNN.
- April 14th - 19th: Replace game controls with keyword outputs from DS-CNN. Troubleshoot issues with keyword recognition and game playability.
- April 19th - End of Semester: Perform final testing of game and work on presentation.

## Sources:
- [Chirravuri, Kuo. Voice Controlled Chess Game on FPGA Using Dynamic Time Warping. MIT, 2008.](https://web.mit.edu/6.111/www/f2008/projects/mikekuo_Project_Final_Report.pdf)
- [Sorensen, Epp, May. A Depthwise Separable Convolutional Neural Network for Keyword Spotting on an Embedded System. EURASIP 2020.](https://www.researchgate.net/publication/342461111_A_depthwise_separable_convolutional_neural_network_for_keyword_spotting_on_an_embedded_system)
- ECE 4550. Lab 4: Accelerating Python with FPGAs - Jupyter Notebooks on the PYNQ-Z1 Board. UVA, 2025.
- [Jach, K. (2008, May 8). PyMaze. Pygame.org. https://www.pygame.org/project/733](https://www.pygame.org/project/733)
