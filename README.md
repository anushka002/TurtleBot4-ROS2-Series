# Intelligent TurtleBot4: Voice-Guided Object Detection and Navigation

---

## Project Overview

Our project transforms the TurtleBot4 and a soon-to-be-mounted MyCobot robotic arm into an intelligent, multi-modal mobile manipulator. Leveraging ROS 2, the system integrates:

- Real-time object detection using YOLOv8.
- Voice command-based navigation and control.
- Obstacle mapping using LiDAR and hazard sensors.
- IMU-based tracking for stability and motion feedback.

The platform provides live visualization through a custom-designed PyQt5-based GUI, aggregating object detection, voice commands, robot velocity, and sensor diagnostics. The final goal is to create a responsive and autonomous system capable of future manipulation tasks using the MyCobot arm.

---

## Research Objective

**How can a mobile robot effectively combine vision, speech, and autonomous navigation to create a responsive and interactive system in real-world environments?**

---

## Key Features

- **Real-Time Object Detection:** YOLOv8 integration for identifying objects using the Oak-D camera.
- **Voice-Guided Control:** Natural interaction through voice commands parsed into actionable navigation tasks.
- **Autonomous Navigation:** ROS2 Navigation Stack integration with obstacle avoidance.
- **Live GUI Dashboard:** Visualizes object detections, voice command status, robot velocity, LiDAR plots, and IMU motion data.
- **Closed-loop Safety Mechanism:** Real-time hazard monitoring ensures robust and safe movements.

---

## ROS2 System Architecture

**Main Nodes:**
- `mic_listener_node`: Captures live microphone audio.
- `command_parser_node`: Parses and structures voice commands.
- `object_detection_node`: Processes camera feed and outputs detections.
- `movement_controller_node`:  Issues movement commands based on goals.
- `gui_publisher_node`: Publishes data streams for GUI visualization.

To-be-done:
  
- `navigation_controller_node`:  Prioritizes between voice commands and object detections.
- `collision_avoidance_node`: Ensures safe path planning based on LiDAR.


**Key Topics:**
- `/rpi_13/oakd/preview/image_raw` — Camera input stream.
- `/yolo_image_raw`  — YOLO object detection Feed.
- `/detected_objects` — YOLO object detections.
- `/voice_text` — Raw voice data.
- `/voice_command` — Parsed voice commands.
- `/rpi_13/cmd_vel` — Robot velocity control.
- `/scan` - Live LIDAR Data feed.
- `/rpi_13/imu` — IMU feedback.


To-be
---

## GUI Features

The GUI built with PyQt5 includes:

- **Live Camera Feed:** Real-time Oak-D frames with object detection overlays.
- **Voice Command Panel:** Displays recognized commands and robot action mappings.
- **Navigation Status:** Robot’s velocity commands and heading.
- **Obstacle Mapping:** LiDAR-based hazard visualization.
- **Sensor Diagnostics:** IMU motion data and hazard detection statuses.

---

## Project Demonstrations

- **Test 1:** Real-time YOLOv8 Object Detection + GUI overlay.
- **Test 2:** Voice-command-based control of TurtleBot4 movement.
- **Test 3 (Planned):** Full autonomy: combining voice input, object detection, and obstacle-aware navigation.
- **Test 4 (Future Scope):** Object manipulation using the MyCobot arm mounted on TurtleBot4.

**Progress Videos:**

- [Real-Time Object Detection Demo](https://youtube.com/shorts/hz7PwtZZgPg?si=9SIvASX0w476p8vp)
- [Voice Command Navigation Demo](https://youtube.com/shorts/DwuBvafB8k8?si=TU1XXYiRUYbrtGBi)

**Live Demonstration Test 1:**

[![Live Demostration Take 1](https://img.youtube.com/vi/DtQAx4mQFKQ/0.jpg)](https://youtu.be/DtQAx4mQFKQ) 


---

## Final Demonstration Plan

- **Setup:** Open indoor space for safe navigation and voice testing.
- **Execution Steps:**
  - Start TurtleBot4 and GUI Dashboard.
  - Perform object detection.
  - Execute user voice commands.
  - Navigate obstacles while maintaining safety.
  - (Future) Pick-and-place task using MyCobot arm.

---

## Future Scope

- **Robotic Arm Integration:** Use MyCobot for pick-and-place tasks based on visual object detection.
- **Adaptive Voice Commands:** Expand vocabulary and robustness against noisy environments.
- **Semantic Scene Understanding:** Move towards task-oriented autonomous planning.

---

## References

1. [YOLOv8 Object Detection](https://github.com/ultralytics/ultralytics)
2. [Speech Recognition in Python](https://pypi.org/project/SpeechRecognition/)
3. [TurtleBot4 ROS2 Tutorials](https://turtlebot.github.io/turtlebot4-user-manual/)
4. [TurtleBot4 Navigation Guide](https://turtlebot.github.io/turtlebot4-user-manual/tutorials/turtlebot4_navigator.html)

---

## Weekly Milestones

| **Week** | **Date** | **Milestone** | **Status** |
|:--------:|:--------:|:--------------|:----------:|
| 7 | Feb 24, 2025 | Finalized project scope and hardware/sensor inventory | ✅ Completed |
| 8 | Mar 3, 2025 | ROS2 environment setup, TurtleBot4 base setup | ✅ Completed |
| 9 | Mar 10, 2025 | YOLOv8 object detection setup with Oak-D camera | ✅ Completed |
| 10 | Mar 17, 2025 | Voice command processing and integration | ✅ Completed |
| 11 | Mar 24, 2025 | Initial GUI development and integration | ✅ Completed |
| 12 | Mar 31, 2025 | Node integration and layered autonomy testing | ✅ Completed |
| 13 | Apr 7, 2025 | TurtleBot4 pipeline testing with live demos | ✅ Completed |
| 14 | Apr 14, 2025 | Final debugging, GUI improvements, and fallback mechanisms | 🔄 In Progress |
| 15 | Apr 21, 2025 | Documentation, final videos, final website submission | 🔄 In Progress |
| 16 | Apr 28, 2025 | 🚀 Final Demonstration | 🔄 In Progress |

---

## Project Impact

- Showcases multi-modal AI integration into real-world robotics.
- Bridges deep learning perception with natural language interfaces.
- Contributes to development of intelligent assistive mobile robots.
- Hands-on training in ROS2, sensor fusion, deep learning, and GUI design.

---

## Advisor

- **Dr. Daniel Aukes**, School for Engineering of Matter, Transport and Energy (SEMTE), Arizona State University

---
## Team Information

- **Project Name:** Intelligent TurtleBot: Deep Learning-Based Object Detection and Voice-Guided Navigation
- **Team Number:** 11
- **Team Members:** Anushka Gangadhar Satav, Adithya Konda, Sameerjeet Singh Chhabra
- **Semester:** Spring 2025
- **University:** Arizona State University
- **Class:** RAS 598 - Experimentation and Deployment of Robots
- **Professor:** Dr. Daniel Aukes
- **Emails:** anushka.satav@asu.edu, akonda5@asu.edu, schhab18@asu.edu

---
