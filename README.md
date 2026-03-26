# STM32 Digital Multichannel Analyzer (MCA)

A low-cost digital spectroscopy system based on STM32 microcontrollers for alpha and gamma radiation detection.

The system implements real-time digital pulse processing (DPP) using a recursive trapezoidal filter and peak detection algorithm. It directly digitizes preamplifier signals and performs on-device signal shaping, energy extraction, and data streaming via USB.

This project is designed with accessibility in mind, aiming to provide an affordable alternative to traditional spectroscopy systems. Future developments include the design of a low-cost charge-sensitive preamplifier and the use of inexpensive photodiodes such as BPX61 photodiode and BPW21R photodiode to significantly reduce system cost and enable wider adoption in educational and research environments.

Features:
• Real-time trapezoidal digital filter
• USB CDC streaming of event energies
• Python GUI for spectrum acquisition
• Adjustable DPP parameters (KGAP, LFLAT, MPZ)
• Works with SiPM, PMT, or semiconductor detectors

Applications:
• Alpha spectroscopy
• Gamma spectroscopy
• Educational nuclear instrumentation
• Low-cost laboratory spectrometers

# STM32 Firmware

This firmware implements a digital multichannel analyzer (MCA) using an STM32 microcontroller.

Functions:

- ADC acquisition using DMA
- recursive trapezoidal digital filter
- peak detection
- USB CDC transmission of event energies

## Build

1. Open project in STM32CubeIDE
2. Build
3. Flash to STM32 board
4. Connect USB

## Commands

The firmware supports runtime parameter control:

TRIG <value>  
END <value>  
KGAP <value>  
LFLAT <value>  
MPZ <value>  
DPP <kgap> <lflat> <mpz>

# Python MCA DAQ

Python program for acquiring and displaying spectra from the STM32 MCA.

Features:

- real-time histogram display
- adjustable spectrum range
- DPP parameter control
- data saving

## Install

py-charm

## Run
