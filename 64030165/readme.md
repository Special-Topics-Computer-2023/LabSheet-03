# 64030165 Ratchanon Busaracome

ในโปรแกรมนี้จะเรียกใช้ function เปิดและปิด LED แทนการตั้งค่าให้เปิดและปิดใน app_main()
```css
#include <unistd.h>      
#include "driver/gpio.h"

const gpio_num_t LED1 = GPIO_NUM_22; 

void LED_Init()
{
    gpio_set_direction(LED1, GPIO_MODE_OUTPUT);
}

void LED_On()
{
    gpio_set_level(LED1, 1);
}

void LED_Off()
{
    gpio_set_level(LED1, 0);
}

void app_main(void)
{
    LED_Init();
    while (true)
    {
        LED_On();
        usleep(500000);
        LED_Off();
        usleep(500000);
    }
}
```

ในการทดลองนี้จะสร้าง file ที่เก็บ method ไว้และเรียก method จาก file นั้นมาใช้ใน main.c

repo - https://github.com/RatchanonBusaracome/Special-Topics-Computer-2023-LabSheet-03

video - https://drive.google.com/file/d/1yl9Ou3uE6NyWXRW7yFEqtTm1MVrd4wYH/view?usp=drive_link
