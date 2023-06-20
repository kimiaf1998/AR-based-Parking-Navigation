# Enhancing Urban Mobility via AR Location-based Parking Navigation System
<!-- <p align="center"> -->
<img src="/Illustrations/PSDet%20Architecture.png" alt="Model Architecture" height="400">
<!-- </p> -->

In this repository, we provide:
- Codes to reproduce all of our results
- Talk about its limitations in real-time content attahement for navigation using ARCore Geospatial API
- [Project report](Project%20Report.pdf) that describes all the methods used in the developement of this project


## Introduction

   The rapid advancements in mobile technologies have generated significant interest in Location-Based Services (LBS). As the reliance on outdoor navigation systems within mobile applications continues to grow, conventional map navigation can be upgraded through the strategic integration of Augmented Reality (AR). Meanwhile, by leveraging landmarks and pathways, AR-based navigation systems hold the potential to enhance user experience to unprecedented levels. 
   This work presents a novel approach combining an automatic camera-based parking space detection method with an AR routing tool, resulting in an interactive driving navigation system. The proposed solution combines Machine Learning methods for parking space detection with advanced navigation systems, offering benefits beyond time-saving for drivers. 
   
## Methodology

The proposed system is comprised of five major components. A Smart Parking Space Detector, a Coordinate System Mapping, a Map and Routing component, an AR-based Interactive Navigation component, and a Server. The system pipeline is demonstrated below.

<img src="/Illustrations/PSDet%20Architecture.png" alt="Model Architecture" height="400">

* Smart Parking Space Detector

   - Detects the location of each parking spot in a parking lot
   - Classifies the occupancy of each spot
   - Uses camera-based Machine Learning methods
   - Images are captured from an overhead CCTV camera
 
     <img src="/Illustrations/PSDet%20Architecture.png" alt="Model Architecture" height="400">
   
* Coordinate System Mapping

   - A mapping component that creates a single coordinate system to work through
   - Establishes a connection between Smart Parking Space Detector's local coordinate system and the global geographic coordinate system (latitude and longitude)
   - Uses camera calibration method to find a transformation matrix
   - Obtains Google Earth's geographic information for parking spots in a parking lot
 
     <img src="/Illustrations/PSDet%20Architecture.png" alt="Model Architecture" height="400">
   
* Map and Routing

   - Determines the optimal route to the closest available parking spot
   - Relies on the Mapbox Navigation SDK which offers a range of features including route calculation and turn-by-turn instructions
   - Leverages the waypoints associated with each step to incorporate visual cues and create an interactive real-time route guidance experience

     <img src="/Illustrations/PSDet%20Architecture.png" alt="Model Architecture" height="400">

* AR-based Interactive Navigation 

* Server
   - Facilitates data transfer between the parking space detection module and the user’s device
   - Is responsible for processing and mapping prediction results obtained from the detection component
   - Sendins the global location of the closest available parking spot to the user’s device for downstream tasks
   - Leverages the Flask framework to ensure smooth communication
   - Uses AWS web service for module deployement
   - Uses Nginx web server to manage incoming HTTP requests and Unicorn3 for process handling 
   - 
<!--
## Inference and Visualization

To run inference on the trained model and get the prediction, run [main.py](main.py). It gets the model predictions given an image and draw predictions on the images to visualize the outputs. 

| ![alt text](/Illustrations/prediction_visualiztion_sample_img1.png) | ![alt text](/Illustrations/prediction_visualiztion_sample_img2.png) |
| ------------ | ------------ |
-->
# Citation

```bibtex
@misc{kimia2023arbased,
      title={Enhancing Urban Mobility via AR Location-based Parking Navigation System}, 
      authors={Kimia Afshari},
      year={2023}
}
```
