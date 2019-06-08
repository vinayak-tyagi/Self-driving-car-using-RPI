# Self-driving-car-using-RPI
Our Major aim for this project is to offline its working(without using the remote servers like AWS, Google Cloud) for ML Model prediction. The reason for that is Latency (Response time/Internet Speed), since project need the quick response (less than a sec) and there are different latencies in different countries or places.

## Hardware
- Remote Control Car (RC Car)
- Raspberry Pi (RPI)
- PI Camera Module
- L298N Dual Motor Controller
- Smartphone External Battery
- 4x AA batteries

## Harware Architecture
![image](https://user-images.githubusercontent.com/39195953/59143889-8b5ea180-89ed-11e9-89c0-78d6827fe9b3.png)

## Software or libraries 
- [Node-red](!https://nodered.org/)
- Tensorflow with Keras
- Pi Camera libraries
- OpenCV
- Various python and important data munching libraries (like:- pandas, pill etc)

## Description
There are 3 file in the project

- `mk_training_data` = This file is used to make training data which are images & CSV file. The images are captured from RPI Camera module and CSV is made from Node-Red.
<b>This file need to exected in RPI itself </b> and one can change the data dir and someone can also saved its data in it's thumbdrive by simply connecting it to RPI and then change the dir path.
<br></br>
`Node-Red` = It is used to control the GPIO pins for making the training data the high and low status of pins drive the motors and finally these status are captured in csv file.
<br></br><b>
It is important to launch both the node-red(which is used to control the gpio) and mk_training_data file(which used to save the camera frames and gpio status in csv) for making training data.
</b>

- `Self driven` = This file is the Main file it can be <b>excecuted anywhere(on Sever or on Local Machine depending on your data size)</b> beacuse it is used for clean the data and training of ANN(Artificial Nural Network) model. Only thing you need do is to change data dir to your data dir which you had made from runing above code(mk_training_data). 
<br></br>
Once the Excetution of this file has been done you will get the training model (.h5 file) as the output in your working dir.

- `rpi_MLModel_interaction` = This file uses the model(.h5 file) and interact with the GPIO's and PI Camera. Hence <b>this file needed to executed in RPI itself</b> beause it take the realtime feed and take the steps accordingly to drive.

## Node-Red UI & Node Flow
![image](https://user-images.githubusercontent.com/39195953/59143953-35d6c480-89ee-11e9-94aa-f1e2bd21fedd.png)
![image](https://user-images.githubusercontent.com/39195953/59143979-86e6b880-89ee-11e9-9b79-34207c300cad.png)

## Snapshorts
![image](https://user-images.githubusercontent.com/39195953/59143850-17bc9480-89ed-11e9-932f-b2c91fa08801.png)
![image](https://user-images.githubusercontent.com/39195953/59143876-4175bb80-89ed-11e9-8ba3-18a5825f05af.png)

## References
- https://github.com/rodrigocava/mrrobot/
- https://github.com/RyanZotti/Self-Driving-Car
- https://projects.raspberrypi.org/en/projects/getting-started-with-picamera
- https://images.nvidia.com/content/tegra/automotive/images/2016/solutions/pdf/end-to-end-dl-using-px.pdf
