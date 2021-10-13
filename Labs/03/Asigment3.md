# Lab 3: EVA MOMENCEAU
Link to your `Digital-electronics-2` GitHub repository:

   [https://github.com/Eva-Momenceau/Digital-Electronics-2](https://github.com/Eva-Momenceau/Digital-Electronics-2)


### Data types in C

1. Complete table.

| **Data type** | **Number of bits** | **Range** | **Description** |
| :-: | :-: | :-: | :-- | 
| `uint8_t`  | 8 | 0, 1, ..., 255 | Unsigned 8-bit integer |
| `int8_t`   | 8 | -128 to 127 | signed 8-bit integer |
| `uint16_t` | 16 | 0 to 65535 | unsigned 16-bit integer |
| `int16_t`  | 16 | -32768 to 32767 | signed 16-bit integer |
| `float`    | 32 | -3.4e+38, ..., 3.4e+38 | Single-precision floating-point |
| `void`     | 0 | none | none |


### GPIO library

1. In your words, describe the difference between the declaration and the definition of the function in C.
   * Function declaration : Used to tell to the compiler that the function exists (name/argument/type of return)
   * Function definition : Tell to the compiler what to do when the function is called

2. Part of the C code listing with syntax highlighting, which toggles LEDs only if push button is pressed. Otherwise, the value of the LEDs does not change. Use function from your GPIO library. Let the push button is connected to port D:

```c
    // Configure Push button at port D and enable internal pull-up resistor
    // WRITE YOUR CODE HERE

    // Infinite loop
    // Configure the green LED as output
    GPIO_config_output(&DDRB, LED_GREEN);
    GPIO_write_low(&PORTB, LED_GREEN);

    GPIO_config_input_pullup(&DDRD, BTN); // Configure the push button at the port D and enable internal pull-up resistor

    // Infinite loop
    while (1)
    {
        if(!(GPIO_read(&PIND, BTN) == 1)) // If the button is pushed 
        {
            GPIO_toggle(&PORTB, LED_GREEN); // Change the state of the LED
            _delay_ms(1000); // Let 1sec befor shecking the state of the push button again
        }
    }
```


### Traffic light

1. Scheme of traffic light application with one red/yellow/green light for cars and one red/green light for pedestrians. Connect AVR device, LEDs, resistors, one push button (for pedestrians), and supply voltage. The image can be drawn on a computer or by hand. Always name all components and their values!

   ![your figure](./Capture.PNG)