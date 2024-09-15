# Hello, I'm Gökdeniz Gülmez 👋

## 🚀 About Me
I'm an aspiring AI & ML researcher, currently honing my skills in system integration and software development. Passionate about leveraging technology to create innovative solutions.

## 📚 My Projects
Here you'll find a variety of projects showcasing my journey in AI and ML. From beginner's experiments to sophisticated models.

## 🎯 My Interests
- 🤖 Artificial Intelligence
- 🧠 Machine Learning
- 🎵 Violin - Currently practicing Bach and more
- 🖌️ Occasionally, I dabble in painting.
- 📺 Avid anime fan, always ready for a good series recommendation.

## 🌱 I’m currently perfecting...
- Autonomous Smart home automation using MLLM (Project J.O.S.I.E.v4o).

<img src="https://github.com/AnderMendoza/AnderMendoza/raw/main/assets/line-neon.gif" width="100%">

## <picture> <img src = "https://github.com/7oSkaaa/7oSkaaa/blob/main/Images/Statistics.gif?raw=true" width = 50px>  </picture> Github Stats
<p align="center"> 
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Goekdeniz-Guelmez&theme=dark&hide_border=True&include_all_commits=True&count_private=True&image_size=auto" /></p>

<br><br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Goekdeniz-Guelmez&&theme=github-compact" alt="Gökdeniz Gülmez's github activity graph"/>

<br><br>

<p align="center"> 
<img src="https://github-readme-streak-stats.herokuapp.com/?user=Goekdeniz-Guelmez&theme=dark&hide_border=True&image_size=auto&image_size=auto" /></p>

<br><br>

<p align="center"> 
<img src="https://github-profile-trophy.vercel.app/?username=Goekdeniz-Guelmez&theme=algolia&column=-1" alt="Gökdeniz Gülmez" /></a> </p>
<hr/>

</div>

<img src="https://github.com/AnderMendoza/AnderMendoza/raw/main/assets/line-neon.gif" width="100%"><br><br>

## My private goal is to create J.O.S.I.E.v4o.
### My own private smart home management MLLM Assistant that can...
- Autonomously control and manage my Smart home with sensors, cameras, LEDs, and all the other products.
- Calling Tools.
- Updating itself Autonomously.
- Having a long-/short-term Memory, and even updating it.
- M-2-M.
- Starting a conversation by itself.
- And much more...]

### Smart home

My advanced smart home model autonomously manages home devices, responds to my commands, and provides real-time monitoring of my home’s environment. All devices, including security cameras, sensors, and other smart home components (lights, thermostats, etc.), are organized in a single unified **devices** section, where each device has a **category** field to distinguish its type (e.g., sensor, security camera, light).

The system can control devices, monitor sensors, and analyse the recent frames from security cameras. Notifications are triggered when events like motion detection or open doors occur, providing real-time updates with the latest information.

#### **Core Functionalities:**

1. **Autonomous Device Control:**
   - J.O.S.I.E. autonomously manages controllable devices like lights and thermostats based on environmental conditions, user-defined schedules and routines, or security triggers.

2. **User-Initiated Device Control:**
   - J.O.S.I.E. processes my commands to control devices like turning on lights, adjusting the thermostat, or locking doors. The system updates the smart home state after executing the command.

3. **Unified Real-Time State Updates:**
   - J.O.S.I.E. outputs real-time updates on the current state of my smart home, which includes all devices (lights, thermostats, sensors, and cameras). Each device has a fields that clarifies whether it’s a sensor, a controllable device, or a security camera.

4. **Proactive Notifications and starting Conversations:**
   - J.O.S.I.E. initiates conversations with the user in response to key events (e.g., motion detection, door left open, temperature change). The notification includes the relevant device information, such as the last frames captured by a security camera or the state of a sensor.

#### **Device Categories:**

Each device in the **devices** section has a **category** field that identifies its type:
- **controllable**: Devices that the model or user can control (e.g., lights, thermostats).
- **sensor**: Passive devices that monitor conditions (e.g., motion detectors, door/window sensors).
- **security**: Security cameras that provide live feeds and snapshots.

#### **Security Camera Integration:**

1. **Live Camera Feeds and Snapshots:**
   - Security cameras continuously monitor the home, providing live feeds and snapshots. The model references the last 2 seconds of frames captured by each camera when events (e.g., motion) occur.
   - Users can request live video streams, and the model will provide the appropriate URL.

2. **Motion Detection and Alerts:**
   - If a camera detects motion, the model captures the last 2 seconds of frames and alerts the user, referencing the image data for review.
   - Example: "Motion detected at the front door. View the last 2 seconds of frames from the front door camera [Snapshot Reference: Front_Door_Camera_Frames]."

#### **Unified Data Structure and JSON Format:**

The **devices** section contains all devices (lights, thermostats, sensors, and security cameras), with a **category** field added to distinguish device types. The **possible_outputs** field for each device is adjusted based on its category, with `null` for passive sensors and specific min/max ranges for controllable devices.

```json
{
  "start_time": "08:00",
  "current_time": "10:00",
  "weather": {
    "current": {
      "temperature": "19.00",
      "humidity": "40",
      "weather": "cloudy",
      "windspeed": "8",
      "wind_direction": "south",
      "feels_like": "18.50",
      "precipitation": "0.0",
      "pressure": "1012",
      "visibility": "10",
      "uv_index": "5",
      "cloud_cover": "25",
      "dew_point": "7.00",
      "sunrise": "06:30",
      "sunset": "18:45"
    },
    "forecast": {
      "hourly": [
        { "hour": "00:00", "temperature": "18.00", "humidity": "42", "windspeed": "6", "weather": "cloudy" },
        { "hour": "01:00", "temperature": "17.50", "humidity": "45", "windspeed": "5", "weather": "cloudy" }
      ]
    }
  },
  "devices": [
    {
      "device_id": "00001",
      "device_name": "light_1",
      "device_type": "light",
      "category": "controllable",
      "room": "living_room",
      "location_description": "northwest corner near the window",
      "state": "off",
      "possible_outputs": {
        "brightness": { "min": 0, "max": 100 },
        "state": ["on", "off"]
      }
    },
    {
      "device_id": "00002",
      "device_name": "thermostat_1",
      "device_type": "thermostat",
      "category": "controllable",
      "room": "bedroom",
      "location_description": "east wall near the door",
      "state": 20.0,
      "possible_outputs": {
        "temperature": { "min": 15, "max": 25 }
      }
    },
    {
      "device_id": "sensor_001",
      "device_name": "motion_sensor_1",
      "device_type": "motion_sensor",
      "category": "sensor",
      "room": "living_room",
      "location_description": "ceiling corner",
      "state": "motion_detected",
      "possible_outputs": null
    },
    {
      "device_id": "sensor_002",
      "device_name": "door_sensor_1",
      "device_type": "door_sensor",
      "category": "sensor",
      "room": "back_door",
      "location_description": "above the back door",
      "state": "door_open",
      "possible_outputs": null
    },
    {
      "device_id": "camera_001",
      "device_name": "front_door_camera",
      "device_type": "security_camera",
      "category": "security",
      "room": "front_door",
      "location_description": "on top of the door",
      "state": "active",
      "frames": "last 2 seconds of frames"
    },
    {
      "device_id": "camera_002",
      "device_name": "backyard_camera",
      "device_type": "security_camera",
      "category": "security",
      "room": "backyard",
      "location_description": "corner of the backyard",
      "state": "active",
      "frames": "last 2 seconds of frames"
    }
  ]
}
```

#### **Device Categories Explained:**

1. **Controllable Devices:**
   - These are devices like lights and thermostats that the model or user can control. The possible outputs for these devices include specific ranges (e.g., brightness, temperature).
   - Example: `"brightness": { "min": 0, "max": 100 }` for lights.

2. **Sensors:**
   - Sensors like motion detectors or door/window sensors are passive monitoring devices. These devices do not have controllable outputs, so their **possible_outputs** field is set to `null`.
   - Example: `motion_sensor` has `possible_outputs: null`.

3. **Security Camera:**
   - Security devices, including cameras, provide real-time monitoring. The model references the last 2 seconds of frames from these cameras when motion is detected or other security events occur. Users are notified of any detected security issues with relevant images.
   - Example: `"frames": "last 2 seconds of frames"`.

#### **Security Features:**

1. **Motion Detection and Camera Snapshots**

2. **Proactive Alerts and Notifications**

3. **Live Camera Feed Access:**

4. **And much much more...**

---

## 🏆 Coursera Certificates
- Introduction to Deep Learning & Neural Networks with Keras
- Deep Neural Networks with PyTorch
- Introduction to Computer Vision and Image Processing
- Building Deep Learning Models with TensorFlow
- AI Capstone Project with Deep Learning
- Machine Learning with Python
- Computer Science: Algorithms, Theory, and Machines
- Linear Algebra for Machine Learning and Data Science
- Probability & Statistics for Machine Learning & Data Science
- Unsupervised Learning, Recommenders, Reinforcement Learning
- Advanced Learning Algorithms
- Supervised Machine Learning: Regression and Classification

<img src="https://github.com/AnderMendoza/AnderMendoza/raw/main/assets/line-neon.gif" width="100%">

## <b> Let's Connect!</b><img src="https://github.com/0xAbdulKhalid/0xAbdulKhalid/raw/main/assets/mdImages/handshake.gif" width ="80">
- [LinkedIn](https://www.linkedin.com/in/gökdeniz-gülmez)

---
⭐️ From [Gökdeniz Gülmez](https://github.com/Goekdeniz-Guelmez)
