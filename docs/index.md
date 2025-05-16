<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<div class="grid.cards.desc" markdown>

<table class="pdf" style="border-style:none;" markdown="1">
<tbody markdown="1">
<tr markdown="1">
<td align="center" width="35%" markdown="block">
[![SparkFun GNSS Combo Breakout - ZED-F9P, NEO-D9S (Qwiic)](https://cdn.sparkfun.com/assets/parts/2/2/7/1/9/22560-_GPS_SparkFun_u-blox_ZED-F9P_NEO-D9S_Combo_Breakout-_01.jpg){ width=90% }](https://www.sparkfun.com/products/22560)

<center>
[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/22560){ .md-button .md-button--primary }
</center>
</td>

<td>
The SparkFun GNSS Combo Breakout - ZED-F9P, NEO-D9S (Qwiic) (GPS-22560) combines the u-blox ZED-F9P multi-band high precision GNSS module with the NEO-D9S L-band GNSS correction data receiver. With a clear view of the sky, especially a clear view to the South, this combo breakout will deliver centimeter-level accuracy positioning without needing separate RTK or NTRIP corrections. An on-board splitter (power divider) allows you to connect both modules to a single L1/L2 L-Band antenna.


</td>
</tr>
</tbody>
</table>
</div class>

The Combo Breakout is designed to work with u-blox's PointPerfect L-band satellite GNSS augmentation service, which provides homogeneous coverage in contiguous USA.

!!! warning
    u-blox provides products and services to "B2B Customers". Only business customers are eligible to register for a Thingstream (PointPerfect) account. You may be required to demonstrate that the use of the combo breakout is in relation to your trade, business, craft or profession. u-blox products and services are not intended for individual consumer use. Please check the [u-blox Service Terms](https://cdn.sparkfun.com/assets/2/5/a/4/f/Service_Terms.pdf) before purchasing hardware.

## Required Materials

Before you begin, you need to think about how you will use the SparkFun GNSS Combo Breakout - ZED-F9P, NEO-D9S (Qwiic).

The Combo Breakout is a very versatile board, combining the u-blox ZED-F9P multi-band high precision GNSS module with the NEO-D9S L-band GNSS correction data receiver.

<center>
[![Hookup for u-center with two USB cables](assets/imgs/22560-GPS-SparkFun-u-blox-ZED-F9P-NEO-D9S-Combo-Breakout-05.jpg){ width="600" }](assets/imgs/22560-GPS-SparkFun-u-blox-ZED-F9P-NEO-D9S-Combo-Breakout-05.jpg)<br>
*Hookup for u-center with two USB cables. (Click to enlarge)*
</center>




If you intend to use [u-blox's u-center (GNSS evaluation software for Windows)](https://www.u-blox.com/en/product/u-center) to configure both the ZED-F9P and the NEO-D9S and log data from the ZED-F9P, all you need to get started is a pair of USB cables and a suitable antenna. u-blox have written an
[excellent application note](https://www.u-blox.com/sites/default/files/documents/NEO-D9S_ZED-F9_Config_SPARTN_AppNote_UBX-22008160.pdf) which shows how to configure both modules using u-center.

<table style="border-style:none">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/17751">
                <center><img src="https://cdn.sparkfun.com/assets/parts/1/6/8/7/4/17587-L1_L2_GNSS_antenna_TOP106-09-1.png" alt="GNSS Multi-Band L1/L2 Surveying Antenna (TNC) - TOP106" height="140"></center>
                <h3 class="title">GNSS Multi-Band L1/L2 Surveying Antenna (TNC) - TOP106</h3>
            </a>
            GPS-17751
        </td>
        <td>
            <a href="https://www.sparkfun.com/products/21281">
                <center><img src="https://cdn.sparkfun.com//assets/parts/2/1/0/6/5/21281-_CAB-_01.jpg" alt="Interface Cable - SMA Female to SMA Male (10m, RG58)" height="140">
                </center>
                <h3 class="title">Interface Cable - SMA Female to SMA Male (10m, RG58)</h3>
            </a>
            CAB-21281
        </td>
    </tr>
</table>

The Combo Breakout has a single female SMA socket for the antenna connection. An on-board splitter (power divider) allows the ZED-F9P and NEO-D9S to share a single antenna. You need an antenna which supports both L1 and L2 GNSS, and which also provides broad coverage of the L-Band for the correction signal. Our TOP-106 antenna is a good choice. It has a TNC connection, so you may also want to purchase a SMA to TNC interface cable and/or a SMA female to male extension cable, depending on your needs:

<table style="border-style:none">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/17833">
                <center><img src="https://cdn.sparkfun.com//assets/parts/1/6/9/8/0/17833-Interface_Cable_-_SMA_Male_to_TNC_Male__300mm_-01.jpg" alt="Interface Cable - SMA Male to TNC Male (300mm)" height="140"></center>
                <h3 class="title">Interface Cable - SMA Male to TNC Male (300mm)</h3>
            </a>
            CAB-17833
        </td>
        <td>
            <a href="https://www.sparkfun.com/products/12861">
                <center><img src="https://cdn.sparkfun.com//assets/parts/9/7/2/9/12861-01.jpg" alt="Interface Cable - SMA Female to SMA Male (25cm)" height="140">
                </center>
                <h3 class="title">Interface Cable - SMA Female to SMA Male (25cm)</h3>
            </a>
            WRL-12861
        </td>
    </tr>
</table>

!!! warning
    While we were able to get the <a href="https://www.sparkfun.com/products/15192">GNSS L1/L2 Multi-Band Magnetic Mount Antenna - 5m (SMA), ANN-MB-00</a> to work with the NEO-D9S in the US, we recommend using a dedicated L1/L2/L-Band antenna for best results. 


## Getting Started with Arduino

<center>
[![Hookup for Arduino using Qwiic](assets/imgs/22560-GPS-SparkFun-u-blox-ZED-F9P-NEO-D9S-Combo-Breakout-06.jpg){ width="600" }](assets/imgs/22560-GPS-SparkFun-u-blox-ZED-F9P-NEO-D9S-Combo-Breakout-06.jpg)<br>
*Hookup for Arduino using Qwiic. (Click to enlarge)*
</center>

It is also possible to power the board and communicate with it using I<sup>2</sup>C by connecting to either of the board's **Qwiic** connectors. SparkFun's [Qwiic Connect System](https://www.sparkfun.com/qwiic) uses 4-pin JST connectors, allowing you to quickly interface your development board to the Combo Board.

Our [u-blox GNSS Arduino Library - v3](https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3) contains a comprehensive set of tried and tested examples that will work
on any Qwiic-enabled development board. There are dedicated examples for the ZED-F9P and NEO-D9S.

You can also use 3.3V Serial (UART) to communicate with both the ZED-F9P and NEO-D9S. Our Arduino Library supports both Serial and I<sup>2</sup>C. (It supports SPI too, but SPI
is not supported on the Combo Breakout).

When choosing a development board, you might want to choose one which has built-in WiFi. The correction data received by the NEO-D9S is encrypted, you need to pass keys to the
ZED-F9P so it can decrypt the data. A WiFi connection will allow you to download the PointPerfect SPARTN encryption keys directly from u-blox's Thingstream IoT service using MQTT.

You might also find a microSD card socket useful for data logging. If you want to log data while you are out in the field, being able to connect a Li-Po battery will be useful too.

These two ESP32 development boards support: Qwiic, Serial, WiFi, microSD and Li-Po.

<table style="border-style:none">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/20168">
                <center><img src="https://cdn.sparkfun.com//assets/parts/1/9/9/6/8/20168Diagonal.jpg" alt="SparkFun Thing Plus - ESP32 WROOM (USB-C)" height="140"></center>
                <h3 class="title">SparkFun Thing Plus - ESP32 WROOM (USB-C)</h3>
            </a>
            WRL-20168
        </td>
        <td>
            <a href="https://www.sparkfun.com/products/19177">
                <center><img src="https://cdn.sparkfun.com//assets/parts/1/8/8/0/0/ESP32_03.jpg" alt="SparkFun IoT RedBoard - ESP32 Development Board" height="140">
                </center>
                <h3 class="title">SparkFun IoT RedBoard - ESP32 Development Board</h3>
            </a>
            WRL-19177
        </td>
    </tr>
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/15081">
                <center><img src="https://cdn.sparkfun.com/assets/parts/1/3/4/3/1/15081-_01.jpg" alt="SparkFun Qwiic Cable Kit" height="140"></center>
                <h3 class="title">SparkFun Qwiic Cable Kit</h3>
            </a>
            KIT-15081
        </td>
        <td>
            <a href="https://www.sparkfun.com/products/14743">
                <center><img src="https://cdn.sparkfun.com//assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg" alt="USB 3.1 Cable A to C - 3 Foot" height="140">
                </center>
                <h3 class="title">USB 3.1 Cable A to C - 3 Foot</h3>
            </a>
            CAB-14743
        </td>
    </tr>
</table>

## Li-Po Battery
<p>For mobile applications, users will want to pick up a <a href="https://www.sparkfun.com/categories/54">single-cell LiPo battery</a> from our catalog. Below, are a few available options:</p>

<table style="border-style:none">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/13855">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/6/2/13855-01.jpg" alt="Lithium Ion Battery - 2Ah" height="140"></center>
                <h3 class="title">Lithium Ion Battery - 2Ah</h3>
            </a>
            PRT-13855
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/13851">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/5/8/13857-01.jpg" alt="Lithium Ion Battery - 400mAh" height="140">
                </center>
                <h3 class="title">Lithium Ion Battery - 400mAh</h3>
            </a>
            PRT-13851
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/13813">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/0/1/13813-01.jpg" alt="Lithium Ion Battery - 1Ah" height="140">
                </center>
                <h3 class="title">Lithium Ion Battery - 1Ah</h3>
            </a>
            PRT-13813
        </td>
    </tr>
</table>

## Jumper Modification

<p>To modify the jumpers, users will need <a href="https://www.sparkfun.com/categories/49">soldering equipment</a> and/or a <a href="https://www.sparkfun.com/categories/379">knife</a>.</p>

<table style="border-style:none">
    <tr>
        <td>
            <a href="https://www.sparkfun.com/products/9325">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/2/8/7/3/09325_9161-Solder_Lead_Free_-_100-gram_Spool-01.jpg" alt="Solder Lead Free - 100-gram Spool" height="140"></center>
                <h3 class="title">Solder Lead Free - 100-gram Spool</h3>
            </a>
            TOL-09325
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/14228">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/1/7/3/14228-01.jpg" alt="Weller WLC100 Soldering Station" height="140">
                </center>
                <h3 class="title">Weller WLC100 Soldering Station</h3>
            </a>
            TOL-14228
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/14579">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg" alt="Chip Quik No-Clean Flux Pen - 10mL" height="140">
                </center>
                <h3 class="title">Chip Quik No-Clean Flux Pen - 10mL</h3>
            </a>
            TOL-14579
        </td>
        <td>
            <a class="thumb" href="https://www.sparkfun.com/products/9200">
                <center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg" alt="Hobby Knife" height="140">
                </center>
                <h3 class="title">Hobby Knife</h3>
            </a>
            TOL-09200
        </td>
    </tr>
</table>


!!! note
    <p>New to jumper pads? Check out our <a href="https://learn.sparkfun.com/tutorials/664">Jumper Pads and PCB Traces Tutorial</a> for a quick introduction!</p>
    <p align="center">
        <a href="https://learn.sparkfun.com/tutorials/664">How to Work with Jumper Pads and PCB Traces<br>
        <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg"></a>
    </p>


## Suggested Reading

As a more professionally oriented product, we will skip over the more fundamental tutorials (i.e. [**Ohm's Law**](https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law) and [**What is Electricity?**](https://learn.sparkfun.com/tutorials/what-is-electricity)). However, below are a few tutorials that may help users familiarize themselves with various aspects of the board.


<table style="border-style:none">
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/61">Installing the Arduino IDE<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/1/arduinoThumb.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/1265">Installing Board Definitions in the Arduino IDE<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/12">Installing an Arduino Library<br>
            <img src="https://cdn.sparkfun.com/c/178-100/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg"></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/908">How to Install CH340 Drivers<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/9/0/8/USB-to-serial_converter_CH340-closeup.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/5">How to Solder: Through-Hole Soldering<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/664">How to Work with Jumper Pads and PCB Traces<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg"></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/8">Serial Communication<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/89">Analog vs. Digital<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/3/7/6/6/0/51c48875ce395f745a000000.png"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/51">Pulse Width Modulation<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/f/9/c/8/a/512e869bce395fbc64000002.JPG"></a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/62">Logic Levels<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/82">I2C<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/8/2/I2C-Block-Diagram.jpg"></a>
        </td>
        <td align="center">
            <a href="https://learn.sparkfun.com/tutorials/16">Serial Peripheral Interface (SPI)<br>
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/6/spiThumb_Updated.jpg"></a>
        </td>
    </tr>
</table>


<center>
<div align="center">
    <div style="top:5px;left:5px;background-color:Gray;position:relative">
        <div style="top:-5px;left:-5px;background-color:#ffffff;position:relative;border:1px solid black;">
            <a href="https://www.sparkfun.com/qwiic"><img src="https://cdn.sparkfun.com/assets/custom_pages/2/7/2/qwiic-logo.png" alt="Qwiic Connect System" title="Qwiic Connect System"></a>
        </div>
    </div>
</div>
</center>

One of the new, advanced features of our Processor Boards is that they take advantage of the [Qwiic connect system](https://www.sparkfun.com/qwiic). We recommend familiarizing yourself with the **Logic Levels** and **I<sup>2</sup>C** tutorials.  Click on the banner above to learn more about [Qwiic products](https://www.sparkfun.com/qwiic).

<center>
    <iframe width="600" height="327" src="https://www.youtube.com/embed/x0RDEHqFIF8" title="SparkFun's Qwiic Connect System" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>
