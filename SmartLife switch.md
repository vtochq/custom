# Adding support for Smartlight switch to Espurna
![SmartLife switch](https://github.com/vtochq/custom/blob/master/SmartLifeSwitch.jpg)

```
#elif defined(VHOME_BLACK_3CH)
    //used pins 2 4 5 12 13 15 16
    //free pins 14

    // Info
    #define MANUFACTURER        "VHOME"
    #define DEVICE              "VHOME_BLACK_3CH"

    // Buttons
    #define BUTTON1_PIN         12
    #define BUTTON2_PIN         5
    #define BUTTON3_PIN         4

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

    #define BUTTON3_MODE        BUTTON_PUSHBUTTON | BUTTON_SET_PULLUP | BUTTON_DEFAULT_HIGH
    #define BUTTON3_PRESS       BUTTON_MODE_NONE
    #define BUTTON3_CLICK       BUTTON_MODE_TOGGLE
    #define BUTTON3_DBLCLICK    BUTTON_MODE_NONE
    #define BUTTON3_LNGCLICK    BUTTON_MODE_NONE
    #define BUTTON3_LNGLNGCLICK BUTTON_MODE_NONE


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
    //#define LED3_PIN            14
    //#define LED3_PIN_INVERSE    1
    #define LED2_MODE         LED_MODE_FOLLOW_INVERSE
    #define LED3_MODE         LED_MODE_FOLLOW_INVERSE
    //#define LED3_MODE         LED_MODE_ON

    #define LED1_PIN            0
    #define LED1_PIN_INVERSE    0

#endif
```
