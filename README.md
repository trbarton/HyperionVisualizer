# Soundreactive WLED via Android Audio Capture

The project aim is to combine the fantastic work by scottlawsonbc on his audio-reactive-led-strip with the work or doktormerlin and his HyperionVisualizer

You should be able to play any audio on the android device and a visualisation is created and sent via UDP over the network to WLED. The packet structure is
the WARLS format set out in the WLED wiki where Byte 0 is the protocol used (WARLS), Byte 2 is the max time for WLED to wait for the next packet and the subsequent bytes
are for LED addresses and colour values

Currently the Rainbow Mood and Rainbow Swirl visualisations work with WLED. Moving forwards I hope to port the logic for scottlawsonbc's visualisations over to Java.
The graphs shown in scottlawsonbc's application would also be a nice touch to implement in the android app.
___

# HyperionVisualizer for Android
HyperionVisualizer for Android is a simple Android app that uses the music played on your mobile phone and visualizes it on your Hyperion using the UDP Listener
![Visualizer](https://i.imgur.com/Ay4C3q4.png)

## Features:
* Currently the app features two visualization options, that resemble the Rainbow Mood and Rainbow Swirl effects. You can set the rate in which the colors change on your own, using a rate of 0 lets you use a static color or rainbow.  
* Setting the color change rate to 0 and using the offset functionality, you can set whatever static color you like.  
* Set the rate at which the visualizer updates on your own. Using a lower rate gives a nice "blocky" visualization effect, while a higher rate gives you a very smooth experience.  
* Use whatever app you want to play your music, it works with all of them (as far as I tested). Spotify, YouTube, PowerAmp. All work fine.  
* Works with all Hyperion Setups, thanks to you being able to set the LED count on your own.

## Usage:
To use this app, you need to first externally start the UDP Listener (using hyperion-remote.sh or the Hyperion App). Then just open the app, enter your details and press start. If you're sick of it, press stop and end the effect.

## Configuration Details:

*   **IP-Address:** IP-Address of your Ambilight System
*   **UDP Port:** Port of your UDP Listener. By default that is Port 2391, but you still have to enter 2391.
*   **Color Switch Rate:** Rate on which the color changes.
*   **LED Count:**  Amount of LED's in your Ambilight setup.
*   **Color Starting offset:**  Offset to start the colors at.
*   **Rate:** The rate on which the visualizer updates in mHz (Milihertz)

## Planned Features:

*   Automatic start and end of the effect using the TCP Interface
*   Rainbow-Swirl-Non-Static effect that not only swirls the colors but also the visualization
*   Making color switch rate independent of rate
*   Better UI
*   Taking care of the service stopping randomly using a foreground service
*   Philips Hue integration
## Sample Videos:
Non-Daylight samples will come soon.

[Sample 1 (featuring cat)](https://www.youtube.com/watch?v=qYQwmd9LVOI)

[Sample 2](https://www.youtube.com/watch?v=Eg247oHoA6I)

## Known Problems:
For known problems, please refer to the issue section.
