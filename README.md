# IS3715 I2C DMX Controller Schematic Example

This repository contains the schematic and implementation guidelines for the **IS3715**, a specialized integrated circuit designed to generate a compliant DMX512-A signal directly from an I2C interface.

---

### 📘 Product Information
* **Product Page:** [I2C DMX Controller IS3715](https://inacks.com/is3715)
* **Datasheet:** [IS3715 Technical Specifications (ISDOC143)](https://inacks.com/is3715_datasheet_isdoc143)

---

### 🚀 Key Benefits of the IS3715
The IS3715 acts as a dedicated DMX controller, offloading the rigorous timing requirements of the MbB and MaB of the DMX512 protocol from the your microcontroller:

* **Autonomous Transmission:** Once channel values are written to the internal 512-byte RAM via I2C, the chip continuously broadcasts the DMX universe at a rock-solid **44 Hz refresh rate**.
* **Glitch Recovery:** Because the chip constantly refreshes the DMX line, any signal interruptions or noise-induced glitches are automatically corrected in the next frame without host intervention.
* **Hardware Synchronization:** Includes a dedicated **SYNC output pin** that pulses high for 100 µs at the start of each DMX Break, allowing for perfect synchronization of multiple universes.
* **Resource Optimization:** Eliminates the need for high-priority UART interrupts and complex timer configurations on your microcontroller.

---

### 🛠️ Evaluation Boards (Plug-and-Play)
To accelerate your development, the following evaluation boards are available with built-in RS485 transceivers and test sliders:

* **For Raspberry Pi:** [Kappa3715Rasp](https://inacks.com/kappa3715rasp)
    * HAT form factor with 3x onboard sliders for immediate DMX testing.
    * Simplifies DMX generation on Linux, where real-time UART timing is often unstable.
* **For Arduino / STM32:** [Kappa3715Ard](https://inacks.com/kappa3715ard)
    * Standard Arduino Shield form factor.
    * Features 3x sliders connected to analog inputs (A1-A3) for easy "fader-to-DMX" prototyping.

---

*For technical support or hardware design review, please visit [inacks.com](https://inacks.com).*
