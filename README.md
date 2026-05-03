## 1. Device Overview

> **Device Description**
> *(在这里用 2 句话极其精炼地概括你的设备：它是做什么的？它的核心技术亮点是什么？)*

**Inspiration & Problem Solving**
* **The Problem:** *(你的设备要解决什么现实痛点？)*
* **The Inspiration:** *(你是怎么想到这个点子的？)*

**Cloud Augmentation**
* *(具体说明你的设备如何利用互联网/云端来增强功能？例如：通过 Azure 实现了远程数据可视化，或利用云端算力进行了数据分析等。)*

---

## 2. System Architecture & Functionality

本设备的核心架构由以下关键组件构成：

| Component Type | Part Details / Function |
| :--- | :--- |
| **Sensors (传感器)** | *(例如：BME280 用于温湿度采集)* |
| **Actuators (执行器)** | *(例如：伺服电机用于物理反馈)* |
| **Microcontroller (主控)** | *(例如：ESP32 / SAMD21)* |
| **Other Components** | *(例如：电源管理模块、特定的通信芯片)* |

**System-Level Block Diagram**
*(用一张高清晰度的系统框图展示硬件与云端的交互流。不要放太复杂的原理图，要放能体现宏观架构的 Block Diagram。)*
![System Block Diagram](./images/diagram.png) 
*(注：之后你需要把图片传到仓库的 images 文件夹，并替换这个路径)*

---

## 3. Engineering Challenges & Solutions

在整个开发周期中，我们在不同层面遇到了挑战，并针对性地进行了解决：

* **Hardware / Firmware Challenges:**
  * **Issue:** *(描述你遇到的硬件bug或底层固件问题)*
  * **Solution:** *(你是怎么Debug的？用了什么测试仪器或代码逻辑解决的？)*

* **Software / Integration Challenges:**
  * **Issue:** *(描述云端接入、Node-RED 配置或软硬件联调时的困难)*
  * **Solution:** *(你采用了什么协议或机制克服了这个瓶颈？)*

---

## 4. Prototype Learnings & Iteration

**Lessons Learned**
* *(写1-2点你在构建和测试原型时学到的核心工程经验，比如“永远要提前规划好电源走线”或者“不要低估无线通信的延迟”)*

**Future Iteration (What I would do differently)**
* *(展示你的工程师思维：如果重来一次，你会如何优化设计？比如换用功耗更低的芯片、优化外壳结构等)*

---

## 5. Next Steps & Course Takeaways

**Path to Production (Next Steps)**
要将这个原型转化为更完善的工程项目，我们计划进行以下优化：
1. *(例如：设计更加紧凑的 4 层 PCBA)*
2. *(例如：完善 Node-RED 的用户交互界面)*

**Course Takeaways (ESE5160)**
通过这门课程的系统学习和全周期的原型开发，我最大的收获是：
*(重点强调你走完了从概念 -> 电路设计(Altium) -> 固件开发 -> 云端部署(Azure/Node-RED) 的全栈硬件开发流程。这是面试官最爱看的一点！)*

---

## 6. Project Links

* 🌐 **Cloud Dashboard:** [Node-RED Instance on Azure](#) *(点击查看实时数据)*
* 🛠️ **Hardware Design:** [Final PCBA on Altium 365](#) *(点击查看完整硬件工程)*

---
*Developed at the University of Pennsylvania (UPenn).*
