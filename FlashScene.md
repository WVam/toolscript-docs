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
|Fade in scene|Boolean|If set to True, will automatically execute [`FadeInScene:[0];`](FadeInScene.md) halfway through the flash.|✗|false|

### Examples:
#### Example #1: Makes the screen flash in a total of 500 milliseconds.
```
1:  Flash:[500];
```

#### Example #1: Makes the screen flash in a total of 500 milliseconds and fades in the scene halfway through, effectively fading in the scene with a flash.
```
2:  Flash:[500|true];
```

### Remarks:
The `Duration` parameter determines the total duration of the flash. This means that fading in and fading out take half the time specified in `Duration` each.
Example: `Duration` is set to 200. Therefore, it will take 100 milliseconds to fade the scene to white and then another 100 milliseconds to fade out the flash again.

---
[Back to overview](index.md)
