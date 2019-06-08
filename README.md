# Self-driving-car-using-RPI
Our Major aim for this project is to localize the working(Does not using the remote sever like AWS, Google Cloud) for ML Model prediction. The reason for that is Latency (Internet speed), since project need the quick responses (less than a sec) multiple times and there may be different latency in different countries or places.


## Description
There are 3 file in the project
- `mk_training_data` = This file is used to make training data which are images & CSV file. The images are captured from rpi camera module and csv is made Node-red commands.
<b>this file need to exected in RPI itself </b> and one can change the data dir and someone can also saved its data in it's thumbdrive by simply connecting it to RPI and then change the dir path
