# Liquid Crystal I2C

## Step 1
Copy i2c-lcd.h and i2c-lcd.c in your STM32Cube projekt

## Step 2
In i2c-lcd.h change -> #include "stm32f1xx_hal.h" suitable for your board

## Step 3
Check in i2c-lcd.c
  - extern I2C_HandleTypeDef hi2c1;
  - #define SLAVE_ADDRESS_LCD 0x4E

## Step 4
Include in your projekt for example:

lcd_init();
lcd_send_string("Hello World");
lcd_put_cur(1,0);
lcd_send_string("First Print");
//lcd_clear();
