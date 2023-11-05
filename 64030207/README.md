# 64030207 Sittinon

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
Repo : https://github.com/Sittinon-Sawatdemongkol/Lab03
Video : https://drive.google.com/file/d/1EyVJb6welcbP2sZs5cduA0TxwRpPUKVo/view?usp=sharing
