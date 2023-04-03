
<div class="grid cards desc" markdown>

<!-- **SparkFun GPS Breakout - Chip Antenna, SAM-M10Q (Qwiic)** (GPS-21834)> -->
-   **SKU:** GPS-21834

    ---

    <figure markdown>
    [![SparkFun GPS Breakout, Chip Antenna - SAM-M10Q (Qwiic)](https://cdn.sparkfun.com/assets/parts/2/1/6/6/4/21834-_GPS-_01.jpg)](https://www.sparkfun.com/products/21834)
    </figure>

-   The [SparkFun SAM-M10Q GPS Breakout](https://www.sparkfun.com/products/21834) features the the SAM-M10Q chip-antenna module from u-blox<sup>&copy;</sup>. The M10Q line is the successor to u-blox&apos;s M8Q found on the [SparkFun GPS Breakout - Chip Antenna, SAM-M8Q (Qwiic)](https://www.sparkfun.com/products/15210) and is a drop-in replacement with updated features to reduce power consumption while also improving performance. The SAM-M10Q can receive up to four GNSS constellations at once which improves time-to-fix and positional accuracy even in areas with limited view of the sky.<br>
    Utilizing our handy Qwiic system, no soldering is required to connect it to the rest of your system. However, the board still breaks out 0.1"-spaced pins for users who prefer a soldered connection or prototyping on a breadboard.

    <center>
    [Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/21834){ .md-button .md-button--primary }
    </center>

</div>

This guide covers the hardware present on this GPS breakout, how to assemble it into a Qwiic circuit and how to use it with the SparkFun u-blox Arduino Library v3.

## Required Materials

To follow along with this guide you will need a microcontroller to communicate with the SAM-M10Q Breakout. Below are a few options that come Qwiic-enabled out of the box:

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/20168">

    <figure markdown>
    ![SparkFun Thing Plus - ESP32 WROOM (USB-C)](https://cdn.sparkfun.com//assets/parts/1/9/9/6/8/20168Diagonal.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/20168">
    **SparkFun Thing Plus - ESP32 WROOM (USB-C)**<br>
    DEV-20168
    </a>

-   <a href="https://www.sparkfun.com/products/18158">
    
    <figure markdown>
    ![SparkFun RedBoard Plus](https://cdn.sparkfun.com//assets/parts/1/7/4/8/7/18158-SparkFun_RedBoard_Plus-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/18158">
    **SparkFun RedBoard Plus**<br>
    DEV-18158
    </a>

-   <a href="https://www.sparkfun.com/products/15574">
    
    <figure markdown>
    ![SparkFun Thing Plus - Artemis](https://cdn.sparkfun.com//assets/parts/1/4/1/7/0/15574-SparkFun_Thing_Plus_-_Artemis-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15574">
    **SparkFun Thing Plus - Artemis**<br>
    DEV-18158
    </a>

-   <a href="https://www.sparkfun.com/products/15444">

    <figure markdown>
    ![SparkFun RedBoard Artemis](https://cdn.sparkfun.com//assets/parts/1/4/0/1/9/15444-SparkFun_RedBoard_Artemis-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15444">**SparkFun RedBoard Artemis**<br>
    DEV-15444
    </a>
</div>

If your chosen microcontroller is not already Qwiic-enabled, you can add that functionality with one or more of the following items:

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/15081">

    <figure markdown>
    ![SparkFun Qwiic Cable Kit)](https://cdn.sparkfun.com//assets/parts/1/3/4/3/1/15081-Qwiic_Cable_Kit_-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15081">
    **SparkFun Qwiic Cable Kit**<br>
    KIT-15081
    </a>

-   <a href="https://www.sparkfun.com/products/14495">
    
    <figure markdown>
    ![SparkFun Qwiic Adapter](https://cdn.sparkfun.com//assets/parts/1/2/5/5/1/14495-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14495">
    **SparkFun Qwiic Adapter**<br>
    DEV-14495
    </a>

-   <a href="https://www.sparkfun.com/products/14352">
    
    <figure markdown>
    ![SparkFun Qwiic Shield for Arduino](https://cdn.sparkfun.com//assets/parts/1/2/3/4/3/14352-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14352">
    **SparkFun Qwiic Shield for Arduino**<br>
    DEV-14352
    </a>

-   <a href="https://www.sparkfun.com/products/16790">

    <figure markdown>
    ![SparkFun Qwiic Shield for Thing Plus](https://cdn.sparkfun.com//assets/parts/1/5/6/9/7/16790-SparkFun_Qwiic_Shield_for_Thing_Plus-05.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/16790">
    **SparkFun Qwiic Shield for Thing Plus**<br>
    DEV-16790
    </a>
</div>

You will also need at least one Qwiic cable to connect your GPS breakout to your microcontroller:

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/17259">

    <figure markdown>
    ![Flexible Qwiic Cable - 100mm)](https://cdn.sparkfun.com//assets/parts/1/6/2/4/6/17259-Flexible_Qwiic_Cable_-_100mm-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/17259">
    **Flexible Qwiic Cable - 100mm**<br>
    PRT-17259
    </a>

-   <a href="https://www.sparkfun.com/products/17260">
    
    <figure markdown>
    ![Qwiic Cable - 50mm](https://cdn.sparkfun.com//assets/parts/1/6/2/4/7/17260-Flexible_Qwiic_Cable_-_50mm-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/17260">
    **Flexible Qwiic Cable - 50mm**<br>
    PRT-17260
    </a>

-   <a href="https://www.sparkfun.com/products/17257">
    
    <figure markdown>
    ![Flexible Qwiic Cable - 500mm](https://cdn.sparkfun.com//assets/parts/1/6/2/4/4/17257-Flexible_Qwiic_Cable_-_500mm-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/17257">
    **Flexible Qwiic Cable - 500mm**<br>
    PRT-17257
    </a>

-   <a href="https://www.sparkfun.com/products/17261">

    <figure markdown>
    ![Flexible Qwiic Cable - Female Jumper (4-pin)](https://cdn.sparkfun.com//assets/parts/1/6/2/4/8/17261-Flexible_Qwiic_Cable_-_Female_Jumper__4-pin_-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/17261">**Flexible Qwiic Cable - Female Jumper (4-pin)**<br>
    CAB-17261
    </a>
</div>

## Optional Materials

If you prefer a soldered connection or want to modify the solder jumpers on this board, you may need some of the products listed below:

<div class="grid cards" markdown align="center">

-   <a href="https://www.sparkfun.com/products/116">

    <figure markdown>
    ![Break Away Headers - Straight)](https://cdn.sparkfun.com//assets/parts/1/0/6/00116-02-L.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/116">
    **Break Away Headers - Straight**<br>
    PRT-00116
    </a>

-   <a href="https://www.sparkfun.com/products/14681">
    
    <figure markdown>
    ![SparkFun Beginner Tool Kit](https://cdn.sparkfun.com//assets/parts/1/2/8/8/3/14681-SparkFun_Beginner_Tool_Kit.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14681">
    **SparkFun Beginner Tool Kit**<br>
    TOL-14681
    </a>

-   <a href="https://www.sparkfun.com/products/9200">
    
    <figure markdown>
    ![Hobby Knife](https://cdn.sparkfun.com//assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/9200">
    **Hobby Knife**<br>
    TOL-09200
    </a>

-   <a href="https://www.sparkfun.com/products/14579">

    <figure markdown>
    ![Chip Quik No-Clean Flux Pen - 10mL](https://cdn.sparkfun.com//assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14579">**Chip Quik No-Clean Flux Pen - 10mL**<br>
    CAB-14579
    </a>
</div>

## Suggested Reading

We designed this board for integration into SparkFun's Qwiic connect system.  Click on the banner below to learn more about the [SparkFun Qwiic Connect System](https://www.sparkfun.com/qwiic).

<div style="text-align: center">
<table>
  <tr>
   <td>
   <div style="text-align: center"><a href="https://www.sparkfun.com/qwiic"><img src="assets/images/Qwiic-registered-updated.png" alt="Qwiic Connect System" title="Click to learn more about the Qwiic Connect System!"></a></div>
   </td>
  </tr>
  <tr>
    <td><div style="text-align: center"><i><a href="https://www.sparkfun.com/qwiic">Qwiic Connect System</a></i></div></td>
  </tr>
</table>
</div>

Before getting started with this Hookup Guide, you may want to read through the tutorials below if you are not familiar with the concepts covered in them or want a refresher. If you are using either of the Qwiic Shields linked above, we recommend reading through their respective Hookup Guides before continuing with this tutorial:

<div class="grid cards hide col-4" markdown align="center">
-   <a href="https://learn.sparkfun.com/tutorials/99">
    <figure markdown>
    ![GPS Basics](https://cdn.sparkfun.com/assets/3/6/6/f/7/50edfc17ce395f7105000000.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/99">**GPS Basics**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/8">
    <figure markdown>
    ![Serial Communication](https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/8">**Serial Communication**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/82">
    <figure markdown>
    ![I2C](https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/82">**I2C**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/16">
    <figure markdown>
    ![Serial Peripheral Interface (SPI)](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/6/spiThumb_Updated.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/16">**Serial Peripheral Interface (SPI)**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/62">
    <figure markdown>
    ![Logic Levels](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/62">**Logic Levels**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/664">
    <figure markdown>
    ![How to Work with Jumper Pads and PCB Traces](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/664">**How to Work with Jumper Pads and PCB Traces**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/815">
    <figure markdown>
    ![Getting Started with u-center](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/8/1/5/u-center.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/815">**Getting Started with u-center**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/684">
    <figure markdown>
    ![Qwiic Shield for Arduino & Photon Hookup Guide](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/6/8/4/Qwic_Shield_Hookup_Guide-05.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/684">**Qwiic Shield for Arduino & Photon Hookup Guide**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/1107">
    <figure markdown>
    ![Qwiic Shield for Thing Plus Hookup Guide](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/1/1/0/7/16138-SparkFun_Qwiic_Shield_for_Thing_Plus-01_Thumb.jpg)
    </figure>
    </a>
    ---
    <a href="https://learn.sparkfun.com/tutorials/1107">**Qwiic Shield for Thing Plus Hookup Guide**
    </a>
</div>