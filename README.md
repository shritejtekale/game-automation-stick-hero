
# Game Automation - Stick Hero

This project focuses on automating the gameplay of the very popular game 'Stick Hero'. The player is challenged to stretch a stick of the right length from one platform to another, so that the avatar avoids falling! 



## :running: In Action

![Stick Hero Demo](https://github.com/shritejtekale/game-automation-stick-hero/blob/main/Stick%20Hero%20Demo.gif)


## :hammer_and_wrench: Installation and Setup

Install the game 'Stick Hero' (by Ketchapp) and a drawing pad of your choice from the Google Play Store. 

#### Steps to setup your Android device:

* Open the Settings app on your phone.

* Navigate to the About Phone section, typically located near the bottom of the list (might be hidden under the 'System' option).

* Tap the Build Number option 7 times consecutively to activate Developer Mode. Now you should see the newly added Developer options in the Settings.

* Access the Developer Options menu and enable the USB Debugging mode.

Then run the following commands on your system to make sure all the required packages are rightly installed:

    pip install import-ipynb
    pip install matplotlib
    pip install pause
    pip install opencv-python
    pip install numpy
    pip install subprocess.run

#### Now let's setup the Windows ADB (Android Debug Bridge):

* Click the link: https://dl.google.com/android/repository/platform-tools-latest-windows.zip 

* This wil start a download. Once the download is complete, extract the ZIP file in a preferred location.

* Navigate to the platform-tools folder and copy it's directory. Search for 'environment variables' on your system and the follow: Environment Variables -> Path (present under User variables) -> New -> Paste the copied path and confirm.

To finally complete the overall setup, connect your Android device to your computer using an USB cable and confirm any pop-ups that appear.

Now open the drawing pad that you installed, naviagte to the platform-tools folder, open the cmd through it and run the command: 

    adv devices
    adb shell input touchscreen swipe 500 500 200 200 1000

This step was performed only to make sure that our devices are properly connected and are able to communicate with each other without any issues. The result of the above command should be a straight line drawn automatically on your drawing pad and your device name being listed in the cmd.

Now that all the setup is complete. Let's get start... :rocket:
## :computer: Implementation 

Let's give it a thought, the avatar likes to wear a red head band on his mission to reach the next platform with a red dot on it! That's it, that's all we need :astonished:

The major steps involved are:

* Capture the screenshot of the device's screen

* Convert it from BGR to RGB and normalise it's dimensions

* Crop the image by tweking the values to only include the avatar and the red destination point (make sure to avoid the cherries)

* Create a canvas of the same size, as of the cropped image and if the pixel matches the red colour set the corresponding pixel to green

* Calculate the distance between the avatar and the destination and create a stick of the corresponding length.

## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## :mega: Feedback

This is my very first GitHub repository so I would love to hear from you any suggestions on how to improve on my work. Also if you have any suggestions, bug reports, or feature requests, please don't hesitate to open an issue on GitHub. Your feedback helps us make this project better for everyone.

Thank you for your support and feedback! :pray:
