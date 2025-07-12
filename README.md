# RhyFeel: Experiencing Music Without Hearing
*2024 Graduation Project – A Multi-Modal Music Translation Platform for the Hearing Impaired*

RhyFeel is an experimental platform that allows hearing-impaired users to **see** and **feel** music in real time through synchronized visual and haptic feedback.

[🔗 Try it out → https://rhyfeel.site](https://rhyfeel.site)

![RhyFeel Poster](./assets/grad-poster.png)

<br>

## Table of Contents

- [Why RhyFeel?](#why-rhyfeel)
- [What It Does](#what-it-does)
- [System Flow](#system-flow)
- [Tech Stack](#tech-stack)
- [Key Values](#key-values)
- [Try It Out](#try-it-out)
- [Contributors](#contributors)
- [Repository Overview](#repository-overview)


<br>

## Why RhyFeel?

Despite growing accessibility technologies, **music remains largely inaccessible** to people with hearing impairments.  
RhyFeel addresses this gap by **translating audio into visual and tactile signals**, offering a new sensory pathway to experience rhythm and beat.

<br>

## What It Does

- **Real-Time Frequency Analysis**  
  Uses Web Audio API to analyze music in 10ms intervals via FFT.

- **3D Music Visualization**  
  Morphs a geometric object in real time based on rhythm and intensity. *(Three.js + Shader)*

- **Haptic Feedback via Wristband**  
  4 vibration motors respond to frequency magnitude. *(ESP32 + PWM control via Web Serial API)*

- **Gesture-Based Controls**  
  Play/pause music using hand gestures. *(MediaPipe Hands: open = ▶️ / closed = ⏸️)*

- **Web-Based Experience**  
  No installation required — works right in the browser.

<br>

## System Flow

1️⃣ **Upload Music**  
  User uploads a local music file (MP3/WAV).

2️⃣ **Audio Analysis (10ms step)**  
  Performs real-time FFT using Web Audio API.

3️⃣ **Output Split**  
- *3D Visualization*  
  → Dynamic icosahedron reacts to beat & mood.  
- *Wristband Vibration*  
  → Vibration intensity modulated by audio strength.

4️⃣ **Gesture Control**  
  Open palm = play / Closed fist = pause  *(MediaPipe Hands, webcam required)*

<br>

## Tech Stack

| Layer        | Technology                                   |
|--------------|----------------------------------------------|
| **Frontend** | React, Three.js, Web Audio API, MediaPipe    |
| **Backend**  | Spring Boot, MySQL, AWS EC2                  |
| **Hardware** | ESP32, 4× ERM Vibration Motors, L9110S Driver |
| **Interface**| Web Serial API (USB connection via browser)  |

<br>

## Key Values

- Enhances **music accessibility** for the hearing-impaired community  
- Delivers an **immersive multi-sensory experience** (visual + tactile)  
- Combines lightweight **hardware and browser-based interaction**  
- Works **anywhere, anytime** with just a browser and a USB connection

<br>

## Try It Out

👉 [https://rhyfeel.site](https://rhyfeel.site)

1. Connect the haptic wristband via USB  
2. Upload your favorite music  
3. Watch and feel — your music come alive!

<br>

## Contributors

- **Dan Kim** (BEng IT Engineering, Sookmyung Women's University, Seoul) 
- **Hansel Lee** (BEng IT Engineering, Sookmyung Women's University, Seoul)  

<br>

## Repository Overview

This GitHub organization contains all repositories related to **RhyFeel**, the 2024 graduation project developed at Sookmyung Women’s University.

🔗 **Organization URL:** [https://github.com/it-graduation-project](https://github.com/it-graduation-project)

#### [`overview-en`](https://github.com/it-graduation-project/overview-en)  
- English-language project summary with README, poster, and documentation.  

#### [`overview`](https://github.com/it-graduation-project/overview)  
- Korean-language overview of RhyFeel. Contains summary documents and metadata.

#### [`frontend`](https://github.com/it-graduation-project/frontend)  
- Frontend React application with real-time music visualization using Three.js and Web Audio API.  
- Includes **hardware integration** via Web Serial API to control haptic feedback through ESP32.
  - Hardware schematics and code for ESP32 + vibration motor system.  
  - Includes motor driver wiring, pinouts, PWM logic, and power setup (12V → 5V step-down).


#### [`backend-analysis`](https://github.com/it-graduation-project/backend-analysis)
- Backend Server, used to analyze FFT and Beat Analysis and return data to the frontend.

#### [`backend`](https://github.com/it-graduation-project/backend) *(🔒 Private)*  
- Original backend built with **Spring Boot** and **MySQL**, deployed on AWS EC2.  
- **Private** due to data security concerns. Handles user management and session authentication via Google OAuth + JWT.


<br>

---
<br>

> *RhyFeel is a graduation capstone project developed at Sookmyung Women’s University in 2024. All rights reserved by the authors.*


