# AutomotiveLaneChangeAssistSystem
for Master of Science in Artificial Intelligence


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

## General Information
The rapid advancement of Autonomous Driving Systems has highlighted the critical need for robust Lane Change Assist frameworks capable of navigating complex highway environments. This thesis proposes a unified perception and decision-making framework that integrates real-time object detection, multi-object tracking, and semantic lane segmentation to enhance the safety and reliability of automated lane change maneuvers. 
The system leverages the state-of-the-art YOLOv11 architecture for high-precision vehicle detection, which represents a significant improvement in spatial localization over previous generations. To ensure temporal consistency and identity persistence, the DeepSORT algorithm is employed to track surrounding agents across consecutive frames, while a UNet architecture generates pixel-level masks to define the ego-lane and adjacent maneuver corridors.
The core of the proposed framework is a deterministic Fusion and Decision Layer that maps tracked object coordinates onto the semantic lane masks to identify potential hazards in the target path. By calculating Time-to-Collision and relative spatial gaps, the system generates a binary safety signal to authorize or inhibit lane change requests. The decision layer employs a simple and comprehendible approach of calculating the lane change decision matrix. The final system achieves high precision and recall in its safety verdicts, effectively mitigating the risks associated with blind-spot occupancy and high-speed closing vehicles. This research provides a repeatable pipeline for future developments in interpretable and modular autonomous perception systems.


## Conclusions
This study demonstrates that a unified perception framework integrating YOLOv11, DeepSORT, and UNet provides a reliable and interpretable foundation for automated LCA systems. By successfully fusing high-fidelity object detection with dense semantic segmentation, the architecture achieves a robust balance between accurate hazard identification and conservative decision-making. The evaluation highlights that while the system maintains high precision in critical safety scenarios, its performance is a vital step toward bridging the gap between raw sensor data and deterministic safety logic.
Ultimately, the research confirms that prioritizing spatial-temporal consistency is essential for building driver trust and ensuring system reliability on the edge. While challenges remain in handling extreme environmental conditions and diverse urban behaviors, this framework establishes a scalable baseline for future autonomous developments. The findings provide a clear pathway for integrating explainable AI into safety-critical maneuvers, ensuring that the next generation of driving assistants is both technologically advanced and fundamentally secure.

## Technologies Used
The experimental studies were conducted in a cloud-based GPU environment to support the training and inference of deep learning models. All tasks were executed on an NVIDIA T4 GPU using the Google Colab platform. This hardware was selected due to its balance of computational performance and accessibility for academic research. The entire pipeline was developed using Python version 3.10 which ensures stable support for the necessary deep learning libraries and data handling tools.
The PyTorch framework was used to implement the YOLO v11 and UNet models for object detection and lane segmentation. The DeepSORT algorithm was also integrated within this environment to manage vehicle tracking across video frames. Supporting libraries such as OpenCV NumPy and Pandas were used for image processing and data management while Matplotlib facilitated the visualization of the experimental results. This software environment provided the necessary infrastructure for the seamless integration of the detection tracking and segmentation modules.


## Contact
Created by [@saumyapriyam] - feel free to contact me!
