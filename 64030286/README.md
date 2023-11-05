นโปรแกรมนี้จะเรียกใช้ function เปิดและปิด LED แทนการตั้งค่าให้เปิดและปิดใน app_main()

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

https://github.com/Pipaul1601/Special-Topics-Computer-2023-LabSheet-03/assets/115067018/7559b60e-464e-47f8-8610-0db8d9af98b3



