Our intented change to the pwm_led_fade.c file was to make the fade up to the high brightness quicker than the fade to the low brightness. Because of this, we modified ++fade to fade=fade+10 in the going up loop, therefore the intensity of the light increments by 10 when it is increasing in brightness, whereas it only decrements by 1 when it is decreasing in brightness; thus, the LED quickly fades to the maximum brightness then relatively slowly fade to the minimum brightness (of the LED being off). 


