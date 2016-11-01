# MD398 Reverse Engineering

Resources for the Tytera (TYT) MD398 (aka Radioddity GD-55).

## General Information

The radio uses a vastly different design than the familiar MD380/MD390. It uses the [AT1846S radio SoC](http://www.auctus.cn/enindex/ptshow.html?id=2).
It is a familiar chip used in many Wouxun/Baofeng model, however to the key difference that this
newer S series provides an IQ baseband interface.

It appears to be using an integrated ARM M7 built into the HR-C3000.

The programming cable is actually a common USB to TTL serial interface (**not** an actual USB device).
It's still not impossible the radio could appear as a DFU usb device for upgrades however.

There is an unused ribbon connector on the front side of the mainboard.

## Connector

The connector used is called _M328+_ (as used on the Motorola GP388 and others), sometimes also called M7. It is 40mm in length.
The audio pinout appears to be identical to other radios using this connector. Two more pins are used for the programming port.
Four more pins are unknown.

## Time Slots

The radio CPS and firmware appear to only allow selecting Time Slot 1. It is possible to modify some xml to enable the CPS to program Time Slot 2.
Doing that however, does not appear to change the behavior of the radio. The radio appears to transmit on both TDMA timeslots with duplicate packets, 
as a Tier I radio would (ie: ETSI 102 361-1 continuous transmission mode).

## Boot Modes

Different boot modes seem to be available:


| PTT | TOP SIDE BUTTON | BOTTOM SIDE BUTTON | EMERGENCY BUTTON | Function |
|:---:|:---------------:|:------------------:|:----------------:| -------- |
| *X* |                 | *X* |    | [Flip + Mirror screen](https://github.com/xSmurf/md398-re/blob/master/teardown/Display_InvertedMirrored.jpg) | 
|     | *X*             | *X* |    | ??? Black screen no chime, upgrade mode? |
|     |                 | *X* | *X* | [GPS Test mode](https://github.com/xSmurf/md398-re/blob/master/teardown/GPS_TestMode.jpg) |
