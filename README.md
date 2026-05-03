# AI Smart Glasses for Elderly Care
**An Always-Available, AI-Powered Assistive Wearable Device**

> **Developed by Team Mind2Matter:** Zicong Zhang & Yibo Wang  
> **Course:** ESE5160 IoT Edge Computing, University of Pennsylvania

---

## 1. Device Overview

> **Device Description**
> This project is a wearable, AI-powered smart glasses system designed specifically for elderly users. It integrates a voice-first AI assistant, real-time fall detection, and environmental awareness to provide hands-free, always-available assistance and safety monitoring.

**Inspiration & Problem Solving**
* **The Problem:** Many existing IoT devices target fitness enthusiasts or smart homes, but few focus holistically on the real needs of elderly users who may struggle with complex interfaces or touchscreens. Falls are also one of the most dangerous risks for this demographic.
* **The Solution:** We built a wearable device that users can interact with naturally using speech. It provides easy access to AI tools, continuously monitors posture for fall detection, and can intelligently analyze the user's surroundings.

**Cloud Augmentation**
* The device acts as an intelligent edge node. By leveraging Wi-Fi connectivity, it offloads heavy processing to the cloud. It uses Cloud APIs for Large Language Models (LLM) to answer complex questions, performs advanced Image processing for object recognition, and streams real-time alerts to a Caregiver Portal during emergencies.

---

## 2. System Architecture & Core Functionality

The device is coordinated by the **Silicon Labs SIWG917 Wi-Fi/BLE MCU**, combining on-device processing with cloud-based intelligence. 

| Subsystem | Key Components & Specifications |
| :--- | :--- |
| **Main Control & Comm** | Silicon Labs SIWG917Y121MGABA (Wi-Fi 6 + BLE 5.3 MCU) |
| **Motion Tracking** | 6-Axis IMU (Accelerometer + Gyroscope) sampled at ≥ 50 Hz |
| **Vision & Audio** | 640×480 Camera Module; I2S Mic (≥ 16 kHz); Bone-conduction/Speaker (≥ 65 dBA) |
| **Power Management** | Single-cell Li-ion Battery (3.7V) with USB-C/5V Charging & Regulation |

**Key Features:**
1. **Voice-First AI Assistant:** Users can ask questions via ASR (Speech-to-Text), and the device replies via TTS (Text-to-Speech) under 15 seconds.
2. **Real-time Fall Detection:** The IMU continuously monitors sudden acceleration/orientation changes. If a fall pattern is detected within 2 seconds, it triggers an audible safety prompt and alerts caregivers if unconfirmed.
3. **Object/Text Assistance:** The camera captures images of surroundings or text, uploading them to the cloud for AI analysis, returning a spoken summary to the user.

**System-Level Block Diagram**
![System Block Diagram](./images/block_diagram.png) 
*(Note: System architecture showing sensor inputs, I2C/I2S routing to the MCU, and cloud interaction via Wi-Fi.)*

---

## 3. PCB Design & Hardware Engineering
*(We designed a custom printed circuit board to fit the strict size constraints of a wearable form factor.)*

**Hardware Highlights:**
* **Wearable Constraints:** Designed to be lightweight and compact to fit an "eyeglasses form factor".
* **Power Routing:** Carefully managed 3.3V and 5V regulated rails to isolate sensitive audio/sensor lines from the RF MCU.
* **Component Selection:** Optimized for low power consumption to maximize the runtime of the single-cell Li-ion battery.

**PCBA 3D Render & Routing:**
![PCBA 3D Render](./images/pcba_3d.png) 
![PCB Routing](./images/pcba_routing.png)

---

## 4. Engineering Challenges & Solutions

* **Challenge 1: Audio / Wake-word Latency**
  * **Issue:** *(留白：写写你们在处理麦克风录音或者音频播放时遇到的困难，比如噪音、延迟)*
  * **Solution:** *(留白：怎么解决的？用了什么缓冲机制？)*

* **Challenge 2: Fall Detection Accuracy**
  * **Issue:** *(留白：写写IMU算法是怎么区分“正常坐下”和“跌倒”的)*
  * **Solution:** *(留白：怎么调试阈值的？)*

* **Challenge 3: Wearable Integration**
  * **Issue:** *(留白：写写电池、摄像头和主板怎么塞进眼镜里的，发热怎么处理的)*
  * **Solution:** *(留白：你的解决方案)*

---

## 5. Prototype Learnings & Future Iteration

**Lessons Learned:**
* *(留白：写一两句最深刻的工程教训，比如硬件选型、或者软硬联调的坑)*

**Future Improvements (Path to Production):**
* **Hardware:** *(例如：采用柔性电路板 FPC 来进一步缩小体积，隐藏在眼镜腿内)*
* **Firmware:** *(例如：加入边缘端的小型唤醒词模型，进一步降低功耗)*

---

## 6. Project Media & Links

**Project Demo Video**
[![Watch the video](https://img.youtube.com/vi/YOUR_VIDEO_ID/hqdefault.jpg)](https://youtu.be/YOUR_VIDEO_ID)
*(Click to watch the real-time AI and Fall Detection Demo)*

**Engineering Resources:**
* 🌐 **Cloud Dashboard:** [Node-RED Instance on Azure](#) *(Caregiver Portal)*
* 🛠️ **Hardware Design:** [Final PCBA on Altium 365](#)

---
*Built with ❤️ for ESE5160 at the University of Pennsylvania.*
