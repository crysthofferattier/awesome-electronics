# Resistor

A resistor is a passive two-terminal electronic component that implements electrical resistance as a circuit element. In electronic circuits, resistors are used to reduce current flow, adjust signal levels, to divide voltages, bias active elements, and terminate transmission lines, among other uses.

## Contents

- [Electronic symbols and notation](#electronic-symbols-and-notation)
- [Color band system](#color-band-system)
- [Color Code](#color-code)
- [Pull Up/Down Resistor](#pull-updown-resistor)

| Property       | Value                       |
|----------------|-----------------------------|
| Unit           | Ohm (Ω)                     |
| Function 	     | Limits current, divides voltage |


![4-band-resistor](/assets/img/resistor.jpg)

### Electronic symbols and notation

- ANSI/IEC

    ![resistor-symbol](/assets/img/resistor-symbol.png)

### Color band system

- The first significant figure of component value (left side)
- The second significant figure (some precision resistors have a third significant figure, and thus five bands).
- The decimal multiplier (number of trailing zeroes, or power of 10 multiplier)
- If present, indicates tolerance of value in percent (no band means 20%)

#### Color code

[Resistor Calculator](https://crysthofferattier.github.io/tools/resistor-calculator)

| COLOR  | FIRST BAND | SECOND BAND | MULTIPLIER           | TOLERANCE |
|--------|------------|-------------|-----------------------|-----------|
| BLACK  | 0          | 0           | x10⁰ (1)              | -         |
| BROWN  | 1          | 1           | x10¹ (10)             | ±1%       |
| RED    | 2          | 2           | x10² (100)            | ±2%       |
| ORANGE | 3          | 3           | x10³ (1K)             | ±0.05%    |
| YELLOW | 4          | 4           | x10⁴ (10K)            | ±0.02%    |
| GREEN  | 5          | 5           | x10⁵ (100K)           | ±0.5%     |
| BLUE   | 6          | 6           | x10⁶ (1M)             | ±0.25%    |
| VIOLET | 7          | 7           | x10⁷ (10M)            | ±0.1%     |
| GREY   | 8          | 8           | x10⁸ (100M)           | ±0.01%    |
| WHITE  | 9          | 9           | x10⁹ (1G)             | -         |
| GOLD   | -          | -           | x10⁻¹ (0.1)           | ±5%       |
| SILVER | -          | -           | x10⁻² (0.01)          | ±10%      |
| PINK   | -          | -           | x10⁻³ (0.001)         | -         |


### Pull Up/Down Resistor

#### Pull UP

A pull-up resistor in electronics is a resistor connected between a **signal line** and a **positive voltage source** (e.g., VCC). 

    Purpose:
    The primary function of a pull-up resistor is to provide a known, high logic level to a signal line when it's not being actively driven by another component, such as a switch or microcontroller. 

How it works:

    When a switch is open (or when no other signal is present), the pull-up resistor pulls the signal line to the positive voltage (VCC). When the switch is closed, the signal line is pulled low (e.g., to ground), and the pull-up resistor has no effect. 

- Benefits:
    - Prevents floating inputs: Without a pull-up resistor, an input pin might be in an undefined state, potentially leading to unpredictable behavior. 
    - Simplified interfacing: It simplifies the interface between switches, buttons, or other devices that may not have a defined signal in their inactive state. 
    - Noise immunity: The pull-up resistor can help reduce the impact of noise on the signal line, as the signal is held at a high level in the absence of noise. 

> Example: Consider a button connected to a microcontroller's input pin. When the button is not pressed, the signal line is pulled high by the pull-up resistor. When the button is pressed, the line is pulled low. 

#### Pull Down

A pull-down resistor ensures a circuit pin is at a low logic level (0V or ground) when no external signal is present. It connects a pin to ground through a resistor, effectively pulling the voltage down to ground in the absence of a driving signal. This is useful in situations where an input pin might otherwise be in an undefined or floating state, which can lead to unpredictable behavior. 

    Purpose:
    Pull-down resistors are used to define a known logic level (low) on a digital circuit input when it's not actively driven by another component. 

- Connection:
    - They are typically connected between the input pin and **ground**.

- Function:
    - When no external signal is present, the pull-down resistor pulls the voltage on the input pin down to ground (0V), ensuring a defined low logic level. 

- Use cases:
    - Pull-down resistors are common in applications like:

- Interfacing with switches: They ensure the input pin is low when a switch is open, and high when it's closed. 

> Digital circuits with open-collector/open-drain outputs: They pull the output low when it's not actively driven