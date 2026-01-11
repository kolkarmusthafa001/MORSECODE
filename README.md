**Morse Code Data Exchange via FPGA Communication Links**

**📌 Project Overview**

This project implements a Morse Code to ASCII Converter using FPGA (Artix-7) and Verilog HDL, with real-time display on a four-digit seven-segment display.
Users input Morse code using a single push button, where short presses represent dots (·) and long presses represent dashes (–). The decoded characters are displayed sequentially, creating a scrolling output.

The design is fully hardware-based and demonstrates core digital design concepts such as clock division, debouncing, finite-state behavior, decoding logic, and display multiplexing.

**✨ Key Features**

- 🔘 Single-button Morse input
- 
- ⏱️ Configurable timing units (1s / 0.5s / 0.25s)
- 
- 🧹 Debounced input for noise-free operation
- 
- 🧠 Binary-tree based Morse decoder
- 
- 🔤 ASCII character generation
- 
- 🔢 4-digit multiplexed seven-segment display
- 
- 🔁 Scrolling character output
- 
- 🔌 Two-FPGA board communication
- 
- 🧩 Modular Verilog architecture


**🏗️ System Architecture**

**FPGA Board 1 – Morse Processing**

- Clock Divider
- 
- Button Debouncer
- 
- Button-to-Morse Converter
- 
Morse-to-ASCII Decoder

**FPGA Board 2 – Display Control**

- ASCII to Seven-Segment Encoder
- 
- Display Shifting Logic
- 
- Multiplexed 4-digit Display Driver

**🛠️ Tools & Technologies Software**

- Xilinx Vivado Design Suite
- 
- Verilog HDL
- 
- RTL Simulation & Synthesis
- 
- On-chip debugging using ILA (optional)

**Hardware**

- EDGE Artix-7 FPGA Development Board (XC7A35T)
- 
- Push Button
- 
- Switches (for timing selection)
- 
- 4-digit Seven-Segment Display

Jumper Wires

**⏲️ Timing Configuration**

Selectable using onboard switches:

| Time Unit | Description           |
| --------- | --------------------- |
| 1.0 s     | Standard Morse timing |
| 0.5 s     | Faster input          |
| 0.25 s    | Very fast input       |


**⚙️ How It Works**

1.User presses the button to input Morse code

2.Press duration determines dot or dash

3.Input is debounced and stored (up to 5 symbols)

4.Inactivity detects end of a letter

5.Morse sequence is decoded into ASCII

6.ASCII character is sent to the second FPGA

7.Character is displayed on the seven-segment display

8.Display shifts for each new letter


**📸 Output**

- Real-time decoded characters
- 
- Scrolling display across 4 digits
- 
- Visual timing feedback using LEDs

**🎯 Applications**

- Digital communication learning
- 
- FPGA-based input decoding systems
- 
- Embedded systems education
- 
- Morse code training tools
