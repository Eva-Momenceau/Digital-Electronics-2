<a name="preparation"></a>
## Preparation tasks (done before the lab at home)

Use schematic of the [LCD keypad shield](../../Docs/arduino_shield.pdf) and find out the connection of LCD display. What data and control signals are used? What is the meaning of these signals?

&nbsp;
VSS 
&nbsp;
VDD
&nbsp;
V0
&nbsp;
RS
&nbsp;
R/W
&nbsp;

&nbsp;







   | **LCD signal(s)** | **AVR pin(s)** | **Description**                                                                                   |
   | :---------------: | :------------: | :------------------------------------------------------------------------------------------------ |
   |        RS         |      PB0       | Register selection signal. Selection between Instruction register (RS=0) and Data register (RS=1) |
   |        R/W        |      gnd       | read from the LCD (RW=1) and Write to the LCD                                                     |
   |         E         |     PB1[9]     | send data to data pins (enable)                                                                   |
   |      D[3:0]       |      none      |  define                                                                                       |
   |      D[7:4]       |    PD[7:4]     | data pins of 8-bits                          

What is the ASCII table? What are the codes/values for uppercase letters `A` to `Z`, lowercase letters `a` to `z`, and numbers `0` to `9` in this table?

| **Char** | **Decimal** | **Hexadecimal** |
   | :------: | :---------: | :-------------: |
   |   `A`    |     65      |      0x41       |
   |   `B`    |     66      |      0x42       |
   |   ...    |             |                 |
   |   `a`    |     97      |      0x61       |
   |   `b`    |     98      |      0x62       |
   |   ...    |             |                 |
   |   `0`    |     48      |      0x30       |
   |   `1`    |     49      |      0x31       |
   |   ...    |             |                 |
