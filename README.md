# Signal Sleeve Detection Template

_NOTE: SDK8.0+ is required._<br />

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

Before we continue, you should take the [Signal Sleeve](https://github.com/ProDCG/PowerPlaySleeveDetection/blob/main/signal-sleeve-template.png) file given and print it out. Once printed out, cut around the edges of the sleeve, and then glue the dark ends together. It is important to note that for a custom signal sleeve to be legal, your team number must be written under it. There are white boxes located underneath each color, where you are supposed to write it. We recommend adding it via a tool like Photoshop or Paint.

Now that we have all the necessary steps required for running and getting pipeline results, we can begin tuning, if the pipeline is not detecting the correct color.

To modify the color ranges, assuming that the pipeline isn't picking it up enough, we can change the existing range values for the lower and upper RGB boundaries for a desired color. <br />
```java
// Lower and upper boundaries for colors
private static final Scalar
        lower_yellow_bounds  = new Scalar(200, 200, 0, 255),
        upper_yellow_bounds  = new Scalar(255, 255, 130, 255),
        lower_cyan_bounds    = new Scalar(0, 200, 200, 255),
        upper_cyan_bounds    = new Scalar(150, 255, 255, 255),
        lower_magenta_bounds = new Scalar(170, 0, 170, 255),
        upper_magenta_bounds = new Scalar(255, 60, 255, 255);
```

When tuned correctly, the box displayed on the screen will alter it's color based on the color picked up. If the box however needs to be moved around and scaled, you can modify the variables seen below to change the position, width, and height.<br />
```java
// TOPLEFT anchor point for the bounding box
private static final Point SLEEVE_TOPLEFT_ANCHOR_POINT = new Point(145, 168);

// Width and height for the bounding box
public static int REGION_WIDTH = 30;
public static int REGION_HEIGHT = 50;
```

After setting up the camera, _(example can be seen in `VisionTest.java`)_ if you want to get the current position stored in an enum, then you can do
```java
sleeveDetection.getPosition()
```

If all the initialization and download steps are completed, you will be able to run the `VisionTest.java` example OpMode and then preview the camera on your driver hub.

## Contact

If you need help with the pipeline or have trouble tuning, don't be afraid to reach out to us! <br />
Discord: ```ProDCG#0641``` <br />
Project: [Repository Link](https://github.com/KookyBotz/PowerPlaySleeveDetection)

For repository specific concerns, feel free to make a fork of this repo, and send a PR.
