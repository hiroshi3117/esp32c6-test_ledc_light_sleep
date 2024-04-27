I based it on "led_basic_example" and added "esp_light_sleep_start" function. But when entering light sleep, LED PWM stops generating.
I referred to some similar questions and added the following settings before entering light sleep:

1. clock source select "RC_FAST"
2. esp_sleep_pd_config(ESP_PD_DOMAIN_RC_FAST, ESP_PD_OPTION_ON);
3. gpio_sleep_sel_dis(LEDC_OUTPUT_IO);

However, PWM generation cannot be maintained during light sleep.
I'm not sure what settings I'm missing in my program that would help me solve this problem.
Thanks!

IDF version: (master)5.4.0
Development board: ESP32-C6-DevKitM-1
Development Platform: Windows, VS Code
