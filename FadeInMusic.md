[Back to overview](index.md)

---
# FadeInMusic (FinM)
---
### Description
Fades in the currently playing music.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of milliseconds it takes to fade in the music.|✓|1000|

### Examples:
#### Example #1: Fading in the music over the span of 3 seconds.
```
1:  FadeInMusic:[3000];
```

#### Example #2: Fading in the music over the span of 1 second.
```
1:  FinM:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 milliseconds).  
The minimum value for `Duration` is 10. If you use a value lower than 10, it will be considered as 10. The only exception to this is 0, which makes the music volume instantly turn back on.

---
[Back to overview](index.md)
