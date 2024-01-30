# virtual-sensor
This is the virtual sensor package to be included in the src file if you want fake cone detection and mapping data

# Installation guide
Copy and paste this entire folder under src file of the autonomous repo

# Initial setup
1: Go to virtual_sensor/virtual_sensor/publisher_member_function.py
2: Find line 43, change the path to the path of "TESTDATA.txt" in your computer. For  me, it is the one shown below. But for you it depends on how you arrange your files. If you are using docker, make sure that you use the directory that is under the docker container (for example: /ws/src/....)
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/eba9c36f-033c-44b5-90bf-297bf9ed7518)

# How to run it
1: colcon build
2: run: ros2 run virtual_sensor talker
You should be able to see bunch of message popping out like this
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/b047595a-425f-456d-b74e-8c5d87bcf6af)

3: run: ros2 run cone_mapping listener
You should be able to see the terminal that you running cone_mapping node showing up bunch of "Listened" like this
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/147dddfb-3f4a-470b-8199-04c3de21ecc2)

# How to generate track
1: Go to virtual_sensor/virtual_sensor/Testcase_Generation
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/a8ebb3d5-1324-43e5-a4c2-a66812bd75ca)

2: Open testcase_generator_track.py

3: If you want to customize your track, you can change the following parameters (don't change anything else, you should not need to). 
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/49992bea-f6f6-467c-9b3e-bc0d7fa42079)

4: Click Run to generate tracks. You should be able to see the following when it is running
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/78d76ccc-b217-442b-b27f-13557ecc3216)

5: You should have your test data stored in a txt file, before you replace this file to TESTDATA.txt that is stored in the parent folder, please ensure that you delete these sections.
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/64a79d19-00e8-408a-9a3b-0835fd0387fa)
Your TESTDATA.txt should look like this:
![image](https://github.com/UOA-FSAE/virtual-sensor/assets/68982001/2b896359-1cf7-4b54-9ec8-1fe8d3ef754b)
(I will update the program to automatically remove these sections for you)
Note:
- Change radius to larger radius if you want you track to be more flat (Use large number to simulate a straight track
- Change file_name if you want your test data being stored in a txt file with a different name.
