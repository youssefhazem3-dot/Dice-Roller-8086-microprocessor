# ATmega32 Stopwatch

## 📌 Overview

This project implements a **digital stopwatch** using the ATmega32
microcontroller and a 16x2 LCD display.\
It was developed as part of the **Digital Systems Interfacing (CSE
362)** course.

The stopwatch provides accurate time measurement in the format:

MM : SS : FF\
(Minutes : Seconds : Hundredths)

The system uses **Timer1 interrupts** for precise timekeeping and
external interrupts for button control.

------------------------------------------------------------------------

## 🎯 Project Features

-   Start, Pause, and Reset functionality
-   16x2 LCD in 4-bit mode
-   Timer1 interrupt-based time calculation (10ms resolution)
-   External interrupts for button control
-   Software debouncing (20ms) for stable button input
-   Tested in Proteus simulation and hardware implementation

------------------------------------------------------------------------

## 🛠 Hardware Components

-   ATmega32 Microcontroller\
-   16x2 LCD (HD44780 compatible)\
-   3 Push Buttons (Start, Pause, Reset)\
-   8 MHz Crystal Oscillator\
-   5V Regulator\
-   Potentiometer (10KΩ)\
-   PCB

------------------------------------------------------------------------

## ⚙️ Software & Tools

-   Embedded C
-   AVR-GCC
-   AVR Libc
-   Atmel Studio
-   Proteus (Circuit Simulation)

------------------------------------------------------------------------

## 🔌 Port Configuration

PORTA (PA0--PA3) → LCD Data (D4--D7)\
PORTB (PB0--PB2) → LCD Control (RS, RW, EN)\
PORTD (PD0) → Reset Button\
PORTD (PD2) → Start/Resume Button\
PORTD (PD3) → Pause Button

------------------------------------------------------------------------

## 🧠 System Design

-   Timer1 generates a 10ms interrupt.
-   Hundredths increment every interrupt.
-   Seconds increment every 100 hundredths.
-   Minutes increment every 60 seconds.
-   LCD updates only when values change to reduce flicker.

------------------------------------------------------------------------

## 🧪 Testing & Results

The system was tested using:

-   Unit testing for LCD initialization and display
-   Interrupt testing for button functionality
-   Timer accuracy verification using external stopwatch

Sample Accuracy Results:

10 Seconds → 00:09:47\
30 Seconds → 00:29:49\
1 Minute → 00:59:50

------------------------------------------------------------------------

## 📂 Source Code

View Source Code:\
https://drive.google.com/file/d/1wSjfPf6yDfUkfpXH-qy9VNJcmakfMwb6/view

------------------------------------------------------------------------

## 👨‍💻 Author
-   Yousef Hazem Hanafi

------------------------------------------------------------------------

## 🔮 Future Improvements

-   Add alarm functionality\
-   Implement countdown timer\
-   Improve timing calibration accuracy\
-   Add EEPROM time storage

------------------------------------------------------------------------

## 📄 License

This project is for educational purposes only.
