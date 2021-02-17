## Electrical

### (THEORITICAL) How to control the voltage of your computer's usb ports ? Is it worth it ?
On a motherboard, USB ports are supplied by hard-coded voltage values. These values can be changed only with an Arduino or by a USB governor tool, but it is recommend not to try this.

<details><summary>Findings and Analysis</summary>

- To control the voltage I have found two ways that are easy and low-cost:

  **Warning**: I am not responsible if you want to reproduce this !

  - Requirements:
    - A [multimeter](https://www.harborfreight.com/7-function-multimeter-98025.html) or a [USB charge doctor](https://www.ebay.com/itm/263297062667)
    - A [USB governor tool](https://www.ebay.com/itm/284183241245)
  - Steps:
    - Find the version of the USB port that you want to control, for example USB 3.0 or USB 2.0, and find its max voltage on [Wikipedia](https://en.wikipedia.org/wiki/USB).
    - Create a circuit that will help you set the max voltage that will be used with the USB governor tool.
    - Once you have set the max voltage on your USB governor tool, run a circuit that supplys your usb port.

- It depends on what you mean by "worth it". For example, this can be useful if you have plug-in a LED and you do not want to spend power unless it's needed. Another use is if you want to try to use this method on mice and keyboards to see if there are any improvements in terms of hertz variation and smoothness. If you are an experienced person and you have 10 dollars this can be worth it.

- Additional research to do: Check the ripple introduction by the PCB with an oscilloscope.

</details>
