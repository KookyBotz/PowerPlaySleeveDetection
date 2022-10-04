# Signal Sleeve Detection Template
This year for PowerPlay, one of the tasks teams have to complete is coming up with a way to detect their custom signal sleeve, placed on top of a cone for the autonomous period. To speed up the process, we created this example signal sleeve template, along with code to show how to use it, and an attached picture of the signal sleeve being used, so that any team can instantly download our code, print out the signal sleeve, and with a little tuning be ready to go for auto. 

Another common problem this plans to help out is give people an easier option for detecting the signal sleeve as opposed to using software like TensorFlow

Here's why:
* TensorFlow can be slow, causing it to not work as well at times
* Without the right tuning and models, might be innacurate
* Rookies are unable to debug it by themselves, leading to it being hard to learn
* If you switch your signal sleeve, you'll have to retrain the model

This template exists to help give rookies a start when it comes to detecting signal sleeves efficiently and effectively.

Use the `VisionTest.java` and `SleeveDetection.java` to get started.

## Getting Started

These instructions will cover how to install the required files, how to setup [EasyOpenCV](https://github.com/OpenFTC/EasyOpenCV), and tune the pipeline.

### Installation

_NOTE: SDK8.0+ is required._<br />
For detailed instructions on how to install the necessary files and setup EOCV, see [EasyOpenCV Installation Setup](https://github.com/OpenFTC/EasyOpenCV)

### Tuning and Usage

Now that all necessary files have been added, download the `VisionTest.java` and `SleeveDetection.java` files above, and drop them into your project files.

Before we continue, you should take the [Signal Sleeve](https://github.com/ProDCG/PowerPlaySleeveDetection/blob/main/signal-sleeve-template.png) file given and print it out. Once printed out, cut around the edges of the sleeve, and then glue the dark ends together.

Now that we have all the necessary steps required for running and getting pipeline results, we can begin tuning, if the pipeline is not detecting the correct color.

To modify the color ranges, assuming that the pipeline isn't picking it up enough, we can change the existing range values for the lower and upper RGB boundaries for a desired color. <br />
![image](https://user-images.githubusercontent.com/55424697/193849790-7ed2f694-1910-45b5-aff8-54bc03d5629e.png)

When tuned correctly, the box displayed on the screen will alter it's color based on the color picked up. If the box however needs to be moved around and scaled, you can modify the variables seen below to change the position, width, and height.<br />
![image](https://user-images.githubusercontent.com/55424697/193850534-87efd16f-0977-4434-a1f4-e35cb64f6fdb.png)

After setting up the camera, _(example can be seen in `VisionTest.java`)_ if you want to get the current position stored in an enum, then you can do
```c++
sleeveDetection.getPosition()
```

If all the initialization and download steps are completed, you will be able to run the `VisionTest.java` example OpMode and then preview the camera on your driver hub.




