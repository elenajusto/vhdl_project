# vhdl_project

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
[![Watch the demo](https://youtube.com/shorts/qv7MFZ6MWjA)