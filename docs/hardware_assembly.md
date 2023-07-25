At a minimum, you will need to attach an external antenna to the SparkFun GNSS Combo Breakout ZED-F9P NEO-D9S, supply 3.3V power, and connect to one of the board's peripherals.

### Attaching an External Antenna

Plug in one of our patch antennas with SMA connector to the GPS board. Secure the connection using the hex nut until it is finger-tight.

<div class="center-block text-center"><a href="assets/imgs/22560-SparkFun_u-blox_ZED-F9P_NEO-D9S_Combo-InstallAntenna.jpg"><img src="assets/imgs/22560-SparkFun_u-blox_ZED-F9P_NEO-D9S_Combo-InstallAntenna.jpg" alt="Finger Tightening the SMA GPS Antenna to the SparkFun GNSS Combo Breakout ZED-F9P NEO-D9S Breakout"></a></div>

<!--
### I<sup>2</sup>C

One method to communicate with the SparkFun GNSS Combo Breakout ZED-F9P, NEO-D9S is through I<sup>2</sup>C. The Qwiic connect system makes it quick and easy to connect the board to your system using a polarized cable. For embedded projects, you can use a Qwiic-enabled Arduino development board like the [ESP32 Thing Plus](https://www.sparkfun.com/products/20168) and its [associated USB cable](https://www.sparkfun.com/products/15425). Then plug a Qwiic cable between the ESP32 Thing Plus and the SparkFun GNSS Combo Breakout ZED-F9P, NEO-D9S.

<center>
[![The ESP32 Thing Plus connected to the SparkFun GNSS Combo Breakout ZED-F9P, NEO-D9S via Qwiic cable.](assets/imgs/22560-GPS-SparkFun-u-blox-ZED-F9P-NEO-D9S-Combo-Breakout-06.jpg){ width="600" }](assets/imgs/22560-GPS-SparkFun-u-blox-ZED-F9P-NEO-D9S-Combo-Breakout-06.jpg)<br>
*The ESP32 Thing Plus connected to the SparkFun GNSS Combo Breakout ZED-F9P, NEO-D9S via Qwiic cable. (Click to enlarge)*
</center>

If you're going to be [soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) to the through hole pins for I<sup>2</sup>C functionality, then just attach the following lines between your chosen microcontroller's I<sup>2</sup>C and the SparkFun GNSS Combo Breakout ZED-F9P, NEO-D9S:

* SDA to SDA
* SCL to SCL
* 3.3V to 3.3V
* GND to GND





### UART

A second method to communicate with the MAX-M10S is through its serial UART. You can directly connect the GPS to the computer by connecting a USB-to-serial converter to the industry standard serial connection (aka the 'FTDI' pinout). In this case, we used an FTDI but you can use another USB-to-serial converter like the CH340. Just make sure to match the silkscreen (GRN to GRN and BLK to BLK). For a secure connection, you&apos;ll need to [solder](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) male header pins or wires to the MAX-M10S.

<div class="center-block text-center"><a href="../assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic_Serial_UART_u-blox.jpg"><img src="../assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic_Serial_UART_u-blox.jpg" alt="USB-to-Serial Converter to MAX-M10S"></a></div>

You could also connect the pins to a microcontroller like the RedBoard Plus as long as the switch for the logic levels are flipped to the 3.3V side before powering the board up. You'll need to do a little bit more work as opposed to using Qwiic connect system. You'll need to attach the following lines between your chosen microcontroller's UART and the MAX-M10S:

* Tx to Rx
* Rx to Tx
* 3.3V to 3.3V
* GND to GND
-->