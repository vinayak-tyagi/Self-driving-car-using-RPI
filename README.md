# Self-driving-car-using-RPI
Our Major aim for this project is to localize the working(Does not using the remote sever like AWS, Google Cloud) for ML Model prediction. The reason for that is Latency (Internet speed), since project need the quick responses (less than a sec) multiple times and there may be different latency in different countries or places.

## Hardware
- Remote Control Car (RC Car)
- Raspberry Pi (RPI)
- PI Camera Module
- L298N Dual Motor Controller
- Smartphone External Battery
- 4x AA batteries

## Software or libraries 
- Node-red
- Tensorflow with Keras
- Pi Camera libraries
- OpenCV
- Various python and important data munching libraries (like:- pandas, pill etc)

## Description
There are 3 file in the project

- `mk_training_data` = This file is used to make training data which are images & CSV file. The images are captured from rpi camera module and csv is made from Node-red UI.
<b>This file need to exected in RPI itself </b> and one can change the data dir and someone can also saved its data in it's thumbdrive by simply connecting it to RPI and then change the dir path.
<br></br>
`Node-Red` = It is used to control the GPIO pins for making the training data the high and low status of pins drive the motors and finally these satutus are captured in csv file with the help of mk_training_data file.
<br></br><b>
It is important to launch the node-red(which is used to control the gpio) and mk_training_data(which used to save the frames and gpio status in csv).
</b>
