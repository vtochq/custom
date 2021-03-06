# Adding support for SmartLife switch to Espurna
My switch looks like this

![SmartLife switch](https://github.com/vtochq/custom/blob/master/SmartLifeSwitch.jpg)

Add definitions to the end of file espurna\code\espurna\config\hardware.h

```
#elif defined(SMARTLIFE_2CH)
    // Info
    #define MANUFACTURER        "SmartLife"
    #define DEVICE              "SMARTLIFE_2CH"

    // Buttons
    #define BUTTON1_PIN         12
    #define BUTTON2_PIN         5

    #define BUTTON1_MODE        BUTTON_PUSHBUTTON | BUTTON_DEFAULT_HIGH
    #define BUTTON1_PRESS       BUTTON_MODE_NONE
    #define BUTTON1_CLICK       BUTTON_MODE_TOGGLE
    #define BUTTON1_DBLCLICK    BUTTON_MODE_NONE
    #define BUTTON1_LNGCLICK    BUTTON_MODE_NONE
    #define BUTTON1_LNGLNGCLICK BUTTON_MODE_RESET

    #define BUTTON2_MODE        BUTTON_PUSHBUTTON | BUTTON_DEFAULT_HIGH
    #define BUTTON2_PRESS       BUTTON_MODE_NONE
    #define BUTTON2_CLICK       BUTTON_MODE_TOGGLE
    #define BUTTON2_DBLCLICK    BUTTON_MODE_NONE
    #define BUTTON2_LNGCLICK    BUTTON_MODE_NONE
    #define BUTTON2_LNGLNGCLICK BUTTON_MODE_RESET

    #define BUTTON1_RELAY       1
    #define BUTTON2_RELAY       2
    #define BUTTON3_RELAY       2

    // Relays
    #define RELAY1_PIN          13
    #define RELAY2_PIN          15
    #define RELAY1_TYPE         RELAY_TYPE_NORMAL
    #define RELAY2_TYPE         RELAY_TYPE_NORMAL

    #define LED2_RELAY          1
    #define LED3_RELAY          2

    // LEDs
    #define LED2_PIN            16
    #define LED2_PIN_INVERSE    1
    #define LED3_PIN            2
    #define LED3_PIN_INVERSE    1
    #define LED2_MODE         LED_MODE_FOLLOW_INVERSE
    #define LED3_MODE         LED_MODE_FOLLOW_INVERSE

    #define LED1_PIN            0
    #define LED1_PIN_INVERSE    0

#endif
```

Then build with flag -DSMARTLIFE_2CH
