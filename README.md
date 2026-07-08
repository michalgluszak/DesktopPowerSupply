# Desktop Power Supply (LM317)

![3D Render](Documentation/Images/3d_render_2.jpg)

## About the Project

The **Desktop Power Supply** is a compact workshop power supply based on the popular and reliable LM317 linear voltage regulator. 

This project was created to provide a simple, cheap, and convenient power source with adjustable voltage, perfect for breadboard prototyping and testing small electronic circuits. The whole device was designed to take up as little space on the desk as possible, while offering everything necessary for the daily work of a hobbyist and engineer.

## Features

* **Adjustable voltage:** Using the LM317 chip and a precision potentiometer allows you to easily adjust the output voltage to the needs of the tested circuit.
* **Built-in voltmeter (Mini Digital LCD):** An integrated display allows for convenient, real-time reading of the set voltage without the need to connect an external multimeter.
  * *Design note:* The footprint of the LCD voltmeter module was prepared based on generally available documentation. Before final PCB production and assembly, I highly recommend buying the physical module to verify the mounting holes and pads.
* **Convenient interface:** A standard DC Jack power socket on the input, a main power switch (Power ON/OFF) with a red status LED, and multiple output pins (pin headers).
* **Thermal management:** Linear voltage regulators generate heat when there are large voltage differences. The project consciously provides enough space to mount an aluminum heatsink for the LM317 chip, which is highly recommended for stable operation under load.

## PCB Technical Specifications

During the PCB design in KiCad, I focused on optimizing power traces and proper heat distribution.

* **Board dimensions:** Very compact format – 55 mm x 36 mm.
* **Power traces (0.8 mm):** Since this is a power supply module, the vast majority of traces carry the main power. Their width was significantly increased (0.8 mm) to safely carry the currents required by the powered circuits and minimize voltage drops.
* **Signal traces (0.25 mm):** Narrower traces were used only for less loaded lines (e.g., the measurement signal for the voltmeter).
* **Ground Planes:** I applied solid ground planes (GND copper pours) on both layers (Top and Bottom). This provides a good return path for the current, reduces noise, and also acts as an additional heatsink to dissipate heat from the components.

## Schematic

![Schematic](Documentation/Images/schematic_2.png)

## PCB Design

Below is a preview of the finished printed circuit board design, showing the optimization of the power traces.

![PCB View](Documentation/Images/PCB_2.PNG)

**Top Layer:**
![PCB Top Layer](Documentation/Images/PCB_r_2.PNG)

**Bottom Layer:**
![PCB Bottom Layer](Documentation/Images/PCB_b_2.PNG)

## Bill of Materials (BOM)

To make ordering parts and soldering easier, I generated an interactive Bill of Materials (BOM). 

👉 **[Open Interactive BOM](https://michalgluszak.github.io/DesktopPowerSupply/Documentation/bom/ibom.html)**

---
*Project created in KiCad 10.0.*