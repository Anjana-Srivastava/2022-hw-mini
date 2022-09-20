Our intented change to the pwm_led_fade.c file was to make the fade up to the high brightness quicker than the fade to the low brightness. Because of this, we modified ++fade to fade=fade+10 in the going up loop, therefore the intensity of the light increments by 10 when it is increasing in brightness, whereas it only decrements by 1 when it is decreasing in brightness; thus, the LED quickly fades to the maximum brightness then relatively slowly fade to the minimum brightness (of the LED being off).

One challenge we faced was with the source code, the type of face was changed from a static int to a static uint16_t. Because this is an unsigned int, it will never pass the condition of fade<0 on line and the LED was not blinking as expected. To fix this, we changed the type back to an int. 


