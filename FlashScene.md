[Back to overview](index.md)

---
# FlashScene (Flash)

---

### Description
Makes the screen flash white. 

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|Specifies how long the flash should take in miliseconds.|✓|200|
|Fade in scene|Boolean|If set to True, will automatically execute [`FadeInScene:[0];`](FadeInScene.md "Fades in the whole screen.") halfway through the flash.|✗|false|

### Examples:
#### Example #1: Makes the screen flash. The flash will last 500 milliseconds.
```
1:  Flash:[500];
```

#### Example #1: Makes the screen flash. The flash will last 500 milliseconds and the scene will appear immediatly halfway through the flash.
```
2:  Flash:[500|true];
```

### Remarks:
The `Duration` parameter determines the total duration of the flash. This means that fading in and fading out each take half the time specified in `Duration`.
Example: If `Duration` is set to 200, it will take 100 milliseconds for the scene to fade to white and then another 100 milliseconds for the scene to fade back in.

---
[Back to overview](index.md)
