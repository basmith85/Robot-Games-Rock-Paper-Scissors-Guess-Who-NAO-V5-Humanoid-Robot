
# Robot Games – NAO Robot Capstone Project

This project was developed as part of a Computer Science capstone course at the University of Kansas. It uses a NAO V5 humanoid robot to play interactive games using image classification and voice interaction.

## Overview

Robot Games is a multi-phase project focused on creating interactive game experiences with the NAO robot. Two games were implemented:

- Rock, Paper, Scissors: Uses hand gesture recognition
- Guess Who: A question-based game using NAO's voice and memory capabilities

This project combines Python, Flask, image classification using MediaPipe, and NAO’s built-in capabilities through Choregraphe.

## Features

- Real-time hand gesture classification from NAO's camera
- Flask server for image classification using MediaPipe
- File-based communication for passing classification results to the robot
- Voice interaction via NAO to guide users through the game
- Modular architecture to support adding future games

## Tech Stack

- Hardware: NAO V5 Humanoid Robot
- Languages: Python 2.7 (for NAO), Python 3 (for Flask server)
- Tools and Libraries:
  - Flask (Python micro web framework)
  - MediaPipe (gesture classification)
  - Choregraphe (robot behavior programming)
  - SFTP for file transfer from NAO to host server

## Architecture Overview

NAO captures a hand image using its camera  
-> Image is transferred to the host machine via SFTP  
-> Flask server classifies the gesture using MediaPipe  
-> Result is saved to a file  
-> NAO reads the result and responds accordingly

## Setup Instructions

### Prerequisites

- NAO V5 robot connected to the same network
- Python 3 installed on the host machine
- Flask and MediaPipe installed: `pip install flask mediapipe`
- Choregraphe installed for uploading and managing robot behaviors

### Running the System

1. Start the Flask server:
   ```
   python3 rps_server.py
   ```

2. Start the Rock Paper Scissors behavior on the NAO robot via Choregraphe.

3. Show a hand gesture to the robot. It captures an image, the server classifies it, and NAO announces the outcome.


## Acknowledgments

- University of Kansas EECS Department
- SoftBank Robotics (NAO platform)
- Google MediaPipe Team
