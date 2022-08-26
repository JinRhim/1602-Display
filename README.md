# 1602-Display
LiquidCrystal 1602 Display Driver


## Hardware 
- Can display 32 ASCII characters 
- 5 x 8 pixels for each character 

<img width="517" alt="image" src="https://user-images.githubusercontent.com/93160540/186827870-8bd7adef-4d40-44a8-b946-0bd5e05491cd.png">

| Ports  | Function |
| ------------- | ------------- |
| V<sub>0</sub>  | LCD brightness |
| Rs (Register Select)  | Low: send command to LCD (setting cursor, clearing display) High: send data to LCD | Rw (Read/Write) | allow to read data from LCD or write data to the LCD | 
| E (Enable) | Low: LCD does not care Rs, Rw, D0~D7. High: Receive Data | 
| D7 - D0 | send character ASCII data: A (0x41) 0100 0001 | 
| A-K | used backlight control | 


#### CGROM
* custom character pattern is saved. 
* custom 5*8 map can be saved at CGRAM


#### DDRAM
* each memory address corresponds to a character position on an attached display
* usually address 00h is the beginning address. 
* address counter is incremented, so the next character will be put at 01h.
<img width="306" alt="image" src="https://user-images.githubusercontent.com/93160540/186831894-8f3ea12c-2850-44b5-aacc-1daccbc8c97f.png">

![image](https://user-images.githubusercontent.com/93160540/186832404-590c1f42-a8bb-4413-a75f-e4a74d077cce.png)

## 8-bit Interface Flowchart 
<img width="559" alt="image" src="https://user-images.githubusercontent.com/93160540/186830348-192826bc-5b52-430e-ba6b-e2700716ca0b.png">


