# VHDL Project: FPGA Interface Experiments

This repository contains a series of VHDL experiments for FPGA development, focusing on different interfacing methods.

## Project Structure

```
.
├── Phase1_GPIO/       # GPIO interface testing
├── Phase2_I2C/       # I2C communication implementation
└── common/           # Shared components and utilities
```

## Phase 1: GPIO Testing
**Description:**

Proof of concept testing to see interfacing with external components via GPIO pins. Here I connected Pin 28 to an LED on a breadboard. When both buttons are pressed or both are unpressed, the LED is off. The LED only turns on when one button is pressed.

**Code:**
```vhdl
entity vhdl_project is
    Port ( 
        input1 : in STD_LOGIC;    -- First input
        input2 : in STD_LOGIC;    -- Second input
        led_out : out STD_LOGIC   -- LED output
    );
end vhdl_project;

architecture Behavioral of vhdl_project is
begin
    -- Simple AND gate implementation
    led_out <= input1 xor input2;
    
end Behavioral;
```

**Video:**

[![Watch the demo](https://img.youtube.com/vi/qv7MFZ6MWjA/0.jpg)](https://youtube.com/shorts/qv7MFZ6MWjA)

## Phase 2: I2C Implementation (In Progress)
**Description:**

This phase will focus on implementing I2C communication with external devices. The goals include:
- Implementing I2C master controller in VHDL
- Setting up communication protocols
- Testing with I2C-compatible sensors/devices

*Details and implementation to be added as development progresses*