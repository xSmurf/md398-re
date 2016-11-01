# MD398 Reverse Engineering

Resources for the Tytera (TYT) MD398 (aka Radioddity GD-55).

## General Information

The radio uses a vastly different design than the familiar MD380/MD390. It uses the [AT1864S radio SoC](http://www.auctus.cn/enindex/ptshow.html?id=2).
It is a familiar chip used in many Wouxun/Baofeng model, however to the key difference that this
newer S series provides an IQ baseband interface.

It appears to be using an integrated ARM M7 built into the HR-C3000.

The programming cable is actually a common USB to TTL serial interface (**not** an actual USB device).
It's still not impossible the radio could appear as a DFU usb device for uprgades however.

## Boot Modes

Different boot modes seem to be available:


| PTT | TOP SIDE BUTTON | BOTTOM SIDE BUTTON | EMERGENCY BUTTON | Function |
|:---:|:---------------:|:------------------:|:----------------:| -------- |
| *X* |                 | *X* |    | Flip + Mirror screen | 
|     | *X*             | *X* |    | ??? Black screen no chime, upgrade mode? |
|     |                 | *X* | *X* | GPS Test mode |
