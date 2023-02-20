# Motion Capture SDK

This is the software development kit (SDK) enabling iOS applications to perform motion capture using [Xsens DOTs](https://www.xsens.com/xsens-dot), which are Bluetooth enabled motion tracking sensors.

The SDK is offered as a Swift Package containing the binary framework that implements the following functionality:
* Handling the connection and disconnection of sensors.
* Setting the update rate and monitoring the effective data rate.
* Resetting the heading of the sensors.
* Assigning segments to sensors.
* Synchronized orientation updates.
* Sensor to segment calibration.
* Battery level monitoring.
* Handling sensor button press.
* Starting and stopping a recording.
* Loading, replaying and trimming a recording.

The SDK offers the recordings as CSV strings which can be saved or distributed by the application.

To install the “MotionCaptureSDK” Swift package in your project, perform the following steps in Xcode:
1. In the Project Editor select your project.
2. Select the tab “Package Dependencies”.
3. Click the + button.
4. In the search bar add the URL to this GitHub repository.
5. Press the “Add Package” button.

The package will be downloaded and added to your project.

By default the SDK can be used without a license, but only allows two sensors two connect. To remove this limitation, a license is required.

>To request a license, please contact [sales@proavatar.io](mailto:sales@proavatar.io?subject=Motion%20Capture%20SDK%20license%20request).

All required functionality is implemented in the `MotionCapture` class. Since there can only be one instance of this class, the singleton design pattern is used and the methods of the class can be accessed using the `MotionCapture.shared` property.

To use this class, place the following import in your Swift files:

```Swift
import MotionCaptureSDK
```

For a complete SDK reference, download the document "[Motion Capture SDK specification](https://docs.google.com/document/d/10cavga-9EazuCiSZettPT0Egue0vIeErZkD-4jK9fjE/preview)".

# Kinematic mode
*The motion capture is performed based on a simplified model comprising the larger segments of a human body to which a sensor can be attached.*

## Segments
In the motion capture as implemented in this package, a simplified kinematic model of a human body is used as illustrated in the figure below. In the figure the names of the segments are given with the motion tracking sensors attached. Note that it is not always necessary to attach sensors to all segments. Depending on what needs to be measured, oftentimes it is sufficient to attach sensors for example only to the lower- or upper-body. This reduces the number of sensors and is less cumbersome for the user.

![Kinematic model](https://docs.google.com/drawings/d/e/2PACX-1vSDT2dcDMyxp9HTz5A_KxZuDo-Ey5ILtMPyORGzIXsfRpzIkVebA863oOVfLgykKGh4lcDd6HgKWD0G/pub?w=190&h=277)



