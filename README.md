# Surveillance-Bot

Remote surveillance and monitoring of our homes has seen a growing need in emerging times. By means of this work, I put forward a surveillance robot which can be integrated into any kind of household. The base controller of the bot will be the powerful Raspberry Pi 3 Model B. A webcam attached to the Pi monitors the area and sends a notification when any trespassing or obtrusion is detected. The camera also possesses face recognition algorithm which will possess the ability to identify the person responsible for the motion triggering. If it is an authorized personnel, the on board voice assistant will start talking with the person. The notification(Alert) will be sent only when it's an unauthorized personnel and will contain pictures clicked of the trespasser and also activate live streaming of the webcam feed. The live streaming ability of the Pi allows the camera feed to be analyzed from any location using internet(Wireless sensor networks). With such a system, every user will feel more sheltered while they're not at their place of residence or when they've left their children and old ones alone at home. It has beeen hosted on AWS and can also be controlled remotely 

This repository end to end framework( Front end, backend and Raspberry pi) for developing a Surveillance bot from the scartch. 


The code Structure is as follows:
1. Client
2. Raspberry Pi control
3. Server


1.The client folder contains all the front end codes for integrating google apis, live track window , remote access(Control window ) etc. 

2.The Raspiberry pi control has 3 submodules:

i. Bot.py which contains the movement control of the bot from the server
ii.camera.py which Takes a photo when the range of the ultrasoic sensor is less than 20cm i.e when motion is detected and then the photo is uploaded to AWS S3 for face recognition. 
iii. livestream.py which sends the live feed to the server. 

3.The server folder has entire backend integration of the framework where it uses flask and Amazon dynamoDB (which is a is a fully managed proprietary NoSQL database service that supports key-value and document data structures and is offered by Amazon.com as part of the Amazon Web Services portfolio) to carry out the tasks. 

Have fun coding and developing your own robot. 
