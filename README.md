# MD398 Reverse Engineering

Resources for the Tytera (TYT) MD398 (aka Radioddity GD-55).

## General Information

The programming cable is actually a common USB to TTL serial interface (**not** an actual USBN device).
It's still not impossible the radio could appear as a DFU usb device for uprgades however.

## Boot Modes

Different boot modes seem to be available:


| PTT | TOP SIDE BUTTON | BOTTOM SIDE BUTTON | EMERGENCY BUTTON | Function |
|:---:|:---------------:|:------------------:|:----------------:| -------- |
| *X* |                 | *X* |    | Flip + Mirror screen | 
|     | *X*             | *X* |    | ??? Black screen no chime, upgrade mode? |
|     |                 | *X* | *X* | GPS Test mode |
