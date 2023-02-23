# Moody-Arduino

Moody-Arduino is the Arduino component of the [`Moody`](https://github.com/tsomic/moody) project. It contains everything that is needed to prepare an Arduino board for the project.

<br/>

## About

With this project it is possible to display a range of facial expressions on an small display. The facial expressions are arranged in a restricted order so that only certain facial expressions can follow one another.

When the Arduino is powered on, it displays a random facial expression that is moving with two frames of animation. After a certain amount of time (between 1 and 2 minutes by default), the display changes to one of the next possible facial expressions.

In addition to these facial expressions, there are also some special facial expressions that are triggered by external events. If the temperature sensor detects a temperature above or below a certain threshold, the "hot" or "cold" facial expression is displayed, respectively. If the knock sensor detects a vibration, the "shock" facial expression appears briefly.

Moody-Arduino is designed to be easily customizable, so you can add your own facial expressions and modify their sequence. You can find out more about that in the [`moody-images`](https://github.com/tsomic/moody-images) and [`moody-mapper`](https://github.com/tsomic/moody-mapper) repositories.

<br/>

## Requirements

To get started with Moody-Arduino, you'll need the following hardware components:

-   An Arduino board (preferably a Seeeduino XIAO)
-   A temperature sensor (preferably a GY-21)
-   A knock sensor (preferably a KY-031)
-   An OLED display (preferably an 1.3" I2C 128x64 OLED display)

<br/>

You'll also need the following libraries:

-   `GY21.h`: A library for the GY-21 Humidity & Temperature Sensor.
-   `Adafruit_SSD1306.h`: A library for controlling SSD1306-based OLED displays.
-   `avr/pgmspace.h`: A library for accessing the flash memory where the images are stored.

<br/>

## Making A Moody

Once you have the necessary hardware and libraries, you can download the code from this repository and flash it onto the Arduino board.

Note that `faces.h` and `facesConfig.h` are automatically generated files and it should not be necessary for you to edit them manually.  
If you want to change the facial expressions and/or mappings, have a look at the [`moody-images`](https://github.com/tsomic/moody-images) and [`moody-mapper`](https://github.com/tsomic/moody-mapper) repositories, where both these files are generated.

The wiring should be pretty straight forward since both the temperature sensor and the display are connected to the I2C pins. Only the knock sensor has its own pin (Pin 6).  
Nonetheless I will upload a circuit diagram once I get to creating it.

Thats basically it! The display will start showing the first facial expression!

<br/>

## Contributing

Contributions are welcome! If you have ideas for new features, find any bugs, or would like to make improvements, please open an issue or submit a pull request.

<br/>

## License

The Moody-Arduino project is licensed under the GNU GPLv3 license. See the [`LICENSE`](https://github.com/tsomic/moody-arduino/blob/main/LICENSE) file for more information.
