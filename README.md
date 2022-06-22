# Motion Capture SDK

This is the software development kit (SDK) to enable a Swift application to perform motion capture using [Xsens DOTs](https://www.xsens.com/xsens-dot), which are Bluetooth enabled motion tracking sensors.

The SDK is offered as a Swift Package that implements the following functionality:
* Handling the connection and disconnection of sensors.
* Setting the update rate.
* Resetting the heading of the sensors.
* Assigning segments to sensors.
* Synchronized orientation updates.
* Sensor to segment calibration.
* Battery level monitoring.
* Handling sensor button press.
* Starting and stopping a recording.
* Loading, replaying and trimming a recording.

The SDK offers the recordings as CSV strings which can be saved or distributed by the application.

For a complete SDK reference, download the document "[Motion Capture SDK specification](https://docs.google.com/document/d/10cavga-9EazuCiSZettPT0Egue0vIeErZkD-4jK9fjE/export?format=pdf)".
