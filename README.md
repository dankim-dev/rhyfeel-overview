# RhyFeel: Experiencing Music Without Hearing
*2024 Graduation Project – A Multi-Modal Music Translation Platform for the Hearing Impaired*

RhyFeel is an experimental platform that allows hearing-impaired users to **see** and **feel** music in real time through synchronized visual and haptic feedback.

[🔗 Try it out → https://rhyfeel.site](https://rhyfeel.site)

![RhyFeel Poster](./assets/grad-poster.png)



## Why RhyFeel?

Despite growing accessibility technologies, **music remains largely inaccessible** to people with hearing impairments.  
RhyFeel addresses this gap by **translating audio into visual and tactile signals**, offering a new sensory pathway to experience rhythm, beat, and emotion.



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



## System Flow

1️⃣ **Upload Music**  
 User uploads a local music file (MP3/WAV).

2️⃣ **Audio Analysis (10ms step)**  
 Performs real-time FFT using Web Audio API.

3️⃣ **Output Split**  
- 🎨 *3D Visualization*  
  → Dynamic icosahedron reacts to beat & mood.  
- 📳 *Wristband Vibration*  
  → Vibration intensity modulated by audio strength.

4️⃣ **Gesture Control**  
 Open palm = play / Closed fist = pause  
 *(MediaPipe Hands, webcam required)*



## Tech Stack

| Layer        | Technology                                   |
|--------------|----------------------------------------------|
| **Frontend** | React, Three.js, Web Audio API, MediaPipe    |
| **Backend**  | Spring Boot, MySQL, AWS EC2                  |
| **Hardware** | ESP32, 4× ERM Vibration Motors, L9110S Driver |
| **Interface**| Web Serial API (USB connection via browser)  |



## Key Values

- Promotes **music accessibility** for the deaf community  
- Offers **immersive sensory experience** (visual + tactile)  
- Integrates lightweight **hardware + web** system  
- Usable **anywhere, anytime** with just a browser and a USB port




## Try It Out

👉 [https://rhyfeel.site](https://rhyfeel.site)

1. Connect the haptic wristband via USB  
2. Upload your favorite music  
3. Watch — and feel — your music come alive


## Contributors

- **Dan Kim** (BEng IT Engineering, Sookmyung Women's University, Seoul) 
- **Hansel Lee** (BEng IT Engineering, Sookmyung Women's University, Seoul)  

---

> *RhyFeel is a graduation capstone project developed at Sookmyung Women’s University in 2024. All rights reserved by the authors.*


