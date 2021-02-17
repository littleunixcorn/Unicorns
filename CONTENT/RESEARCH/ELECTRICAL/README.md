## Electrical

### (THEORITICAL) How to control the voltage of your computer's usb ports ? Is it worth it ?
On a motherboard, USB ports are supplied by hard-coded voltage values.These values can be changed only with an Arduino or by a USB governor tool, though nobody try this.

<details><summary>Findings and Analysis</summary>

- For control the voltage I have found two ways that are easy and low-cost:

  **Warning**: I am not responsible if you want to reproduce this !
  - Requirements:
    - A [multimeter](https://www.harborfreight.com/7-function-multimeter-98025.html) or a [USB charge doctor](https://www.ebay.com/itm/263297062667).
    - A [USB governor tool](https://www.ebay.com/itm/284183241245).
  - Steps:
    - Get the version of the USB port that you want to control and get its max voltage from [Wikipedia](https://en.wikipedia.org/wiki/USB).
    - Create a circuit that will help you to set the max voltage that you have to use with the USB governor tool.
    - Once your USB governor tool is at the right value do a circuit that supply your usb port.

- It depends on what you mean by "worth it", this can be useful if you are plug-in a LED and you do not want to spend power for nothing or even if you want to try to use this on mice and keyboards to see if there is any improvements in term of hertz variation, smoothness.
If you are not a beginner and you have 10 bucks this is worth it.

- Additional research to do : Check the ripple introduction by the PCB with an oscilloscope.

</details>
