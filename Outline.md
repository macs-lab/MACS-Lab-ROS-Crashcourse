Objective of the course: learn how to use ROS to design and program robust robotic control systems.

#### Keywords
- Pathplanning
- Taskplanning
- Sensors
	- Vision cameras
	- RGBD cameras
- Classical computer vision
- Kinematics
- Rigid-body Motions
- Networking (LAN)
- Robot setup
- *Machine-Learning*
- *Reinforcement-Learning*


1. (OVERVIEW) MACS Lab Ecosystem
	1. Network of computers, robots, sensors
	2. Overview of things that will be learned
2. Anatomy of a Robot (Chess Robot Example?)
	1. Designing robots
		1. Rodney Brooks, *A Robust Layered Control System For A Mobile Robot*, 1986
	2. Before we jump into ROS we want to give a big picture of how a MACS Lab robotic system works
	3. Show and describe control system flow and logic
		1. Task planning, image processing, etc.
	4. Robot control system design exercise - pick and place? - Breitenberg robot?
	5. How is it all implemented?
		1. Pubs/subs, services, etc.
3. ROS Part 1
	1. Introduction to ROS
		1. Broad description of what ROS is: central nervous system
			1. Compare control system diagram and task-achieving diagram with ROS system diagram
		2. What kinds of robots have been programmed with ROS?
	3. Tutorials
		Examples end up coming together to make some kind of interesting ROS system.
		1. Publisher/Subscriber example
			1. What are pub/sub and ROS msg?
			2. Supply image publisher with fun example image.
			3. They write the subscriber in an already provided file (#TODO)
		2. Service example
			1. Why do we need services? Jusitfy in comparison to pub/sub.
			2. Example server/client pair (#TODO)
		3. ROS Packages
			1. What is a package?
			2. Best practices:
				1. How to split up your code into logical packages
				2. scripts for python code, README.md, docs folder for documentation, msg, srv, etc., CATKIN_MAKE
4. Image Collection and Processing and Intro to CV
	1. Intro to OpenCV
	2. Supply publisher node that connects to Mako camera and sends stream of images. Include option for simulated camera which sends downloaded video frames.
	3. #TODO write code in subscriber callback that performs different kinds of image processing in order to recognize object (possibly). Setup controlled area in room with different objects, one yellow duck for them to identify
		1. Converting between grayscale, RGB, HSV, etc.
		2. Gaussian blur
		3. Thresholding
		4. cv_bridge for converting to ROS Image message