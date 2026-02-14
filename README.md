# Smart Digital Pen for Seamless Handwriting Digitization

## Overview
The Smart Digital Pen is a portable system that captures handwriting motion using an inertial measurement unit (IMU) and converts it into digital text in real time. The system works wirelessly and allows people to write on any surface—or even in the air—while their handwriting is instantly digitized, recognized, and stored.

The project combines embedded hardware, wireless communication, and intelligent software to bridge the gap between traditional handwriting and digital workflows.

---

## Problem Statement
Handwriting remains one of the most natural and widely used methods of communication in education, professional environments, and daily life. However, converting handwritten content into digital format is still a challenge. Existing solutions such as graphic tablets, stylus-enabled screens, and smart notebooks are often expensive, require special surfaces, or depend on proprietary hardware.

Many users need a simple, portable, and affordable solution that allows them to write naturally while still benefiting from digital storage, editing, and sharing. Additionally, current systems often lack real-time recognition, voice feedback, and gesture-based interaction.

The Smart Digital Pen addresses these challenges by providing a low-cost, wireless, and surface-independent solution that captures handwriting motion and converts it into digital text in real time.

---

## Key Features
- Real-time motion capture using IMU sensor
- Wireless Bluetooth Low Energy (BLE) connectivity
- Surface-independent writing (any surface or air)
- Digital stroke rendering on a virtual canvas
- Handwriting-to-text conversion using OCR
- Gesture-based controls (triple-click to recognize text)
- Voice feedback using text-to-speech
- Voice command support
- Automatic text saving with timestamps
- Modular hardware–software architecture

---

## System Architecture

### Hardware Module
The hardware module is responsible for capturing hand motion and transmitting it to the computer.

**Components:**
- XIAO BLE microcontroller (nRF52840)
- LSM6DS3 IMU sensor
- Push-button input
- Bluetooth Low Energy communication

**Functions:**
- Reads motion data from the IMU
- Converts motion into cursor movement
- Sends data wirelessly via BLE HID
- Detects click and gesture inputs

---

### Software Module
The software module processes the cursor input, displays strokes, and performs handwriting recognition.

**Functions:**
- Digital canvas for stroke rendering
- Image preprocessing
- Handwriting recognition using OCR
- Text display, voice output, and file storage

---

## Technologies Used

### Hardware
- XIAO BLE (nRF52840 microcontroller)
- LSM6DS3 IMU sensor
- Bluetooth Low Energy (BLE)
- I2C communication protocol

### Firmware
- Arduino C/C++
- Adafruit Bluefruit BLE library

### Software
- Python 3.x
- Tkinter (GUI)
- OpenCV (image processing)
- Tesseract OCR (v4+)
- pytesseract
- SpeechRecognition
- gTTS (text-to-speech)
- playsound3
- NumPy

---

## System Workflow
1. User writes using the smart pen.
2. IMU detects motion and sends data to the microcontroller.
3. Microcontroller converts motion into cursor movement.
4. Cursor draws strokes on the digital canvas.
5. User performs a triple-click gesture.
6. OCR is triggered to recognize the handwritten strokes.
7. Recognized text is:
   - Displayed on screen
   - Spoken aloud
   - Saved to a text file

---

## Repository Structure


---

## Installation and Setup

### Hardware Setup
1. Connect the LSM6DS3 IMU to the XIAO BLE via I2C.
2. Connect the push-button to the designated GPIO pin.
3. Open Arduino IDE.
4. Select the correct board (XIAO BLE).
5. Upload the `air_mouse.ino` firmware.
6. Pair the device with your computer via Bluetooth.

---

### Software Setup

#### Step 1: Install Python
Install Python 3.8 or later.

#### Step 2: Install Dependencies
Run the following command:

#### Step 3: Install Tesseract OCR
Download and install Tesseract:
https://github.com/tesseract-ocr/tesseract

Ensure the Tesseract path is correctly set in the Python script.

#### Step 4: Run the Application


---

## Controls

### Pen Controls
- Movement: Cursor movement and drawing
- Single click: Mouse click
- Triple click: Trigger OCR recognition

### Keyboard Shortcuts
- C: Clear canvas
- X: Run OCR
- S: Save recognized text
- Q: Quit application

### Voice Commands
- “Clear” → Clears the canvas
- “Run” or “Start” → Runs OCR
- “Save” → Saves recognized text
- “Exit” → Closes the application

---

## Current Implementation Status
- Hardware motion capture: Completed
- BLE cursor control: Completed
- Digital canvas rendering: Completed
- OCR-based text recognition: Completed
- Voice feedback and commands: Completed
- Integrated end-to-end system: Functional prototype

### Pending Improvements
- Motion smoothing and calibration
- Recognition accuracy improvements
- Power optimization
- Ergonomic pen casing
- Extensive real-world testing

---

## Innovation Highlights
- Surface-independent writing
- Low-cost alternative to commercial smart pens
- Real-time handwriting digitization
- Gesture and voice-based interaction
- Modular and scalable architecture

---

## Applications
- Digital note-taking
- Smart classrooms
- Assistive technology
- Meetings and presentations
- Field data collection

---

## Intellectual Property Notice
The design and core implementation of this Smart Digital Pen are protected under a **design patent**.  
This repository is provided for demonstration and evaluation purposes only.

Unauthorized copying, reproduction, modification, or commercial use of the design or code is not permitted without prior written consent from the project owners.

---

## Authors
- Anjana m s
- Akshay k prasad
- Alok shaji
- Adithya k b

---

## Contact
For collaboration, licensing, or academic inquiries, please contact the project team.

---

## License
All rights reserved.  
This project is protected under a design patent and is not open source.
