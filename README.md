# GD32F103VC_IS61LV256AL #

Use IS61LV256AL in GD32F103VC

---------------------------------------

## 1. Crystal oscillator is 12MHz ##

## 2. Schematic ##

![Chip connection](Doc\IS61LV256AL-Schematic.png)

## 3. Debug problem ##

I can only use the first `256 Bytes` of `IS61LV256AL`. I guess the reason maybe is that `AIP74HC573` is a `8 bits` Latches, but `GD32F103VK`'s data bus and address bus are **multiplexed**.

The chip `IS61LV256AL` need waveforms is as below:

![read cycle](Doc\IS61LV256AL-read-cycle.png)
![write cycle1](Doc\IS61LV256AL-write-cycle1.png)
![write cycle2](Doc\IS61LV256AL-write-cycle2.png)