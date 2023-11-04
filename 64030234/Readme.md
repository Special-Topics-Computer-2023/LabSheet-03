# นางสาวกุลธิดา เกษร

# code
```css
#include <unistd.h>
#include "driver/gpio.h"

const gpio_num_t LED1 = GPIO_NUM_23;

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
# วิดีโอ
https://drive.google.com/drive/folders/13nKOF6hwrXKrUk9fCsaq77UcJk86Rwkp

# Repo Project

https://github.com/KUNTIDA234/LabSheet-03
