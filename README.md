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

