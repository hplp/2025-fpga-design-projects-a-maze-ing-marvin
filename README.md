# Project_Template

## FPGA Project Group 4

## Team Members:
- Lisa Berlizova
- Troy Harmon
- Tessa Heick

## Project Title:
### a-MAZE-ing Marvin: A voice activated maze game run on a PYNQ-Z1 board via TinyML network.


## Project Description:
Online games have become an essential aspect of modern entertainment, offering experiences that
range from expansive multiplayer worlds to minesweeper on Google Chrome. However, many games rely
on the physical dexterity of players, requiring consoles, keyboards, or motion detection systems. This can
be challenging for individuals with limited mobility or finger strength. Thus, voice controlled movement
in tandem with a single button system can provide an alternative, making simpler games more accessible
to a wider audience.
This project looks to integrate an existing maze game built with the Pygame library4 with a
keyword detection system to create an accessible game run on an FPGA (the PYNQ-Z1 to be exact). It
will use the onboard microphone and button system to capture audio from the player, which is then used
by the DS-CNN to identify keywords, which will act as direction to move the player’s character through
the maze. The FPGA will be running Jupyter Notebook via ethernet to display the game on a nearby
monitor.

## Key Objectives:
- Implement a DS-CNN that is capable of identifying kewords used in a maze game, such as "up", "down", etc.
- Launch the network on the PYNQ-Z1 board, utilizing the onboard microphone and ethernet connection.
- Integrate a publicly available maze game with our system.

## Technology Stack:
(List the hardware platform, software tools, language(s), etc. you plan to use)
- PYNQ-Z1 Board
- Ethernet wire
- PC
- Monitor
- Jupyter Notebook (Python)
- Publicly available maze game: LINK

## Expected Outcomes:
(Describe what you expect to deliver at the end of the project)
We will deliver a locally run, voice-controlled maze game.
ADD MORE

## Tasks:
(Describe the tasks that need to be completed. Assign students to tasks)
Lisa: Build and test DS-CNN
Troy: Interface maze game with our system
Tessa: Implement microphone control, interface DS-CNN with board
All: Test game, add easter eggs!

## Timeline:
(Provide a timeline or milestones for the project)
April 4th - April 18th: Get game working 
April 19th - End of Semester: Test game
