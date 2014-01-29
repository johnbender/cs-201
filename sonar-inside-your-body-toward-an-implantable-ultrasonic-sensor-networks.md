# Sonar Inside Your Body: Towards Implantable Ultrasonic Sensor Networks

Tommaso Melodia

- intrabody wireless networks and sensors
 - networks of implantable mini wireless sensing and actuating devices
 - communicate wirelessly with external devices
 - communicate with gateway

- applications
 - in-vivo monitoring
 - sensing and actuation
 - robotic microsurgery
 - nano medicine
- examples
 - interocular pressure modeling (glaucoma)
 - heart monitoring
  - many sensors
  - many defib
  - much better than pacemaker using more subtle actuation
 - automated drug admin
  - measure input administer drug
  - insulin pump etc
 - micro surgery
  - less invasive
 - pill sized digestible cameras
 - malicious agent detecting
  - cancer
 - bone growth
 - replacement for organs

 - sub cubic millimeter ocular pressure
 - google smart lens

- how are networks created
 - em waves
  - soft tissues
  - water medium of tissue is not good for transmission
 - RF
  - poor signal in water media
  - heat up tissues
  - not well understood the impact
  - body doesn't work well with antenna

- acoustic waves
 - previous research in underwater research
 - medical imaging
 - low attenuation
 - safe with intensity controls
 - low speed
 - transducers can be efficiently coupled

- work
 - investigate ultrasonic
 - check wideband ultrasonic
 - ultrasonic software testbed
 - modeling interference

- ultrasonic communication
 - mechanical pressure waves
 - same as sound
 - > 20kh are above human hearing
 - attenuation
  - exp log
  - low freq == less attenuation
 - propagation
 - issues with human tissues !
  - reflections
  - scattering
 - kidney scatters
 - transducers
  - low freq
  - acoustic radiation pattern
  - main lobe determines direction
  - small devices => high freq (size)
 - communication distance
  - > cm 10mhx

- channel modeling
 - two ways to model
  - deterministic propagation models
  - statistical models
 - Deterministic
  - equation used with tools
  - modeling with different materials and the result of attenuation
  - model for kidney, bone, etc
 - Statistical
  - model path loss (measurements)
  - model small scale fading, how the signal fluctuates
  - model channel input response
  - phantom body parts to build model
   - eg, kidney


 - low complexity
 - low power
 - low duty cycle
 - waveform diversity (different communications)
 - not much coordination (avoid MAC etc)

 - impulsive transmissions
  - do not overlap in time
  - less interference between communication of many different nodes

- Signaling scheme
 - short (100ns) pulses
 - 0 bit is close to start of chip time
 - 1 bet at the end
 - frame contains one pulse
 - hopping and randomness to prevent collision
  - trading off between bandwidth and resiliency

 - Rate and energy tradeoff
  - rate is inversely proportional to the spread, frame length, and chip duration
  -

- Mac layer
 - time hopping
 - rate adaptation
 - tradeoffs

- Rate max
 - solvable non linear optimization problem
 - adapt rate for power
 - common control channel
 - private dedicated data channel
 - control exchange for ack

- ultrasonic communication
 - software defined radio to build platform
 - host machine
 - GNU Radio
 - transducers
  - underwater not good enough (too low)
  - medical ultrasound
  - transducers for fault detection in material

 - physical layer not going to work in software
 - overload host and hardware
 - physical layer on FPGA

- MAC layer needed to be on fpga
- move to HDL
- hybrid
- custom logic for handling packet layer/etc

- Performance evaluation
 - how did it work in kidney
 - interference hurts throughput
 - number of packets does not decrease

- optimization of packet size
 - increased size reduce reliability
 - longer packets use the channel more efficiently with less acks

- developed simulator
 - wave level
 - bit level
 - packet level
 - simulated network issues for many nodes

- Similar to underwater modem
 - 1.38mbits per second for close distances
 - around 500kb for range of 100m
 - promise for video surveillance
 -

- Future work
 - omnidirectional vs directional
 - arrays of transducers
 - can nanonetworks use ultrasonic transducers
 - photoacoustic effect
  - heat
 - Small device implementation
  - few mm
 - wearables (glasses, watches, avoid rf/em waves)
 -
