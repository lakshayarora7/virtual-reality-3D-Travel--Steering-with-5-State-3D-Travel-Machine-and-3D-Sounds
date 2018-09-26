# virtual-reality-3D-Travel--Steering-with-5-State-3D-Travel-Machine-and-3D-Sounds

![Alt text](screenshot1.png?raw=true "3D Virtual Environment")
![Alt text](screenshot2.png?raw=true "3D Travel")

Due to size restrictions on github, placed code at https://drive.google.com/drive/folders/1CjGLk1tl5Kcy6Odbuh10bLS9VH5L4OjW?usp=sharing. 

Developd a 3D travel technique (Steering) with five meaningful interaction states. Used the Vive prefab’s 'Real World Simulator' to ensure that all five interaction states of 3D travel technique are properly functioning and can be used with the HTC Vive. The Vive prefab is part of 5UDE, a package developed by Professor Ryan McMahan at FIVE labs at UTD. Copyright information inside the zip file.

Used the 5UDE's sound script to assign 5 unique and realistic 3D sounds withing the virtual environment. Sounds were imported from various sources on the internet. Used the Vive prefabs's 'Real World Simulator' to ensure that the sounds are realistic when using the steering travel technique to move about the virtual environment.

Package Requirements:
1. Steam VR (downloaded from Unity Asset Store)
2. 5UDE: a package designed by Professor Ryan McMahan (University of Texas at Dallas), contains a real worl simulator along with HTC Vive inputs.

To run the scene:
1. Install Unity.
2. Click on Assets/LivingArea.unity
3. Click on play button in game bar.

Sources for virtual objects used:

S. No.	Object 	    URL
1.		  Couch	      https://assetstore.unity.com/packages/3d/props/furniture/modern-sofa-27370

2.		  Flower Vase	https://assetstore.unity.com/packages/3d/vegetation/flowers/ornamental-flower-set-11920

3.		  Centre Table (Round)	https://assetstore.unity.com/packages/3d/props/furniture/wooden-table-and-chair-18996

4.		  Laptop	    https://assetstore.unity.com/packages/3d/props/electronics/free-laptop-90315

5.		  Painting	  https://assetstore.unity.com/packages/3d/props/interior/paintings-free-44185

6.		  Books	      https://assetstore.unity.com/packages/3d/props/interior/books-3356

7.		  Wall Lamp	  https://assetstore.unity.com/packages/3d/props/simple-wall-lamp-69411

8.		  Guitar    	https://assetstore.unity.com/packages/3d/props/acoustic-guitar-21037

9.		  Clock	      https://assetstore.unity.com/packages/3d/props/interior/clock-4250

10.		  Study Table	https://assetstore.unity.com/packages/3d/props/furniture/folding-table-and-chair-pbr-111726

11.		  Panasonic Phone 	https://www.cgtrader.com/items/624708/download-page

12.		  Alarm Clock 	https://www.cgtrader.com/items/274658/download-page



Sources for sounds used:

S. No.	Sound Type  	             URL
1.		  Wall Clock Ticking Sound	https://www.soundjay.com/clock-sounds-1.html

2.		  Laptop(FAN)	              https://www.freesoundeffects.com/free-track/fan1-426973/

3.		  Alarm timer sound	        https://www.audiomicro.com/alarm-clock-bell-runs-down-short-household-house-alarm-clock-bell-runs-down-short-free-sound-effects-44725

4.		  Laptop Low battery sound	https://www.youtube.com/watch?v=CbLPEHeVHu

5.		  Phone ringing sound 	    https://www.audiomicro.com/phone-electric-rings-once-household-phone-electric-rings-once-free-sound-effects-44731





3D Travel 5-State Machine: 

![Alt text](3D%20Travel%205%20State%20Machine.png?raw=true "3D Travel 5-State Machine")

 
LEGEND (How to use it with HTC Vive)
1: joystick.GetAxis().y > 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
2: joystick.GetAxis().x < 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
3: joystick.GetAxis().y < 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
4: !button.GetPress()
5: joystick.GetAxis().y > 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
6: joystick.GetAxis().y > 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
7: joystick.GetAxis().y > 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
8: joystick.GetAxis().x > 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
9: space.transform.position += joystick.GetAxis().y * tracker.transform.forward * speed * Time.deltaTime
10: joystick.GetAxis().x < 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
11: !button.GetPress()
12: joystick.GetAxis().x < 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
13: joystick.GetAxis().x > 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
14: joystick.GetAxis().x < 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
15: joystick.GetAxis().y < 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
16: space.transform.position -= joystick.GetAxis().x * tracker.transform.right * speed * Time.deltaTime
17: !button.GetPress()
18: joystick.GetAxis().y < 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
19: joystick.GetAxis().x > 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress()
20: joystick.GetAxis().y < 0.0f && (Math.Abs(joystick.GetAxis().y) > Math.Abs(joystick.GetAxis().x)) && button.GetPress()
21: space.transform.position -= joystick.GetAxis().y * tracker.transform.forward * speed * Time.deltaTime
22: !button.GetPress()
23: joystick.GetAxis().x > 0.0f && (Math.Abs(joystick.GetAxis().x) > Math.Abs(joystick.GetAxis().y)) && button.GetPress() 
24: space.transform.position += joystick.GetAxis().x * tracker.transform.right * speed * Time.deltaTime
