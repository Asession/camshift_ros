Camshift tracker
================
    This is a ROS version of the camshift tracker, modified from the example 
of opencv.
    You select a color objects such as your face and it tracks it.
    This subscribs from "/image" topic for reading images, and publishes the 
position and size of target to "/TargetPositionSize" topic or "/roi" topic.
    The position and size have been normalized.
    Note: For windows, you should install python first, then install opencv2 
and numpy.
Usage:
------
    Give excute permission to camshift_node.py by
	chmod +x scripts/camshift_node.py

    Insure the "/image" topic has data, then run
        roscore
        rosrun camshift camshift_node.py

    If you have installed usb_cam package, you can test by running
        roslaunch camshift camshift_test.launch
Keys:
-----
    ESC/q	- exit
    b    	- toggle back-projected probability visualization
    s		- save roi to file
    l		- load roi from file to calculate hist
