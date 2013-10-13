# Anatasios Mourikis, High-Precision Localization with Cameras and Inertial Sensors

Professor Mourikis began his talk by introducing some reasons why robot positioning (localization) is difficult. He discussed GPS and how it's the gold standard for localization, but more importantly he covered the scenarios in which GPS won't work. It turns out there is a large diversity of very important robotics applications that make positioning with GPS impossible like underground, indoors, underwater, or even heavily wooded areas.

After setting the stage for the importance of non-GPS localization research, he described the primary tools that researchers are currently using. First and possibly most importantly is the IMU, or Inertial Measurement Unit. IMU's provide velocity, orientation, and gravitational force information. When coupled with a camera the two form a solid foundation for determining position from a starting point with a relatively low accumulation of error.

Accumulated error was an important focus of Professor Mourikis's talk. Even the best IMU's and image algorithms introduce some level of information uncertainty into the calculation of position. Much of his work focuses on ..
