[Back to overview](index.md)

---
# FadeOutMusic (FoutM)
---
### Description
Fades out the currently playing music.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of milliseconds it takes to fade out the music.|✓|1000|

### Examples:
#### Example #1: Fading out the music over the span of 3 seconds.
```
1:  FadeOutMusic:[3000];
```

#### Example #2: Fading out the music over the span of 1 second.
```
1:  FoutM:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 milliseconds).  
The minimum value for `Duration` is 10. If you use a value lower than 10, it will be considered as 10. The only exception to this is 0, which instantly mutes the music volume.

---
[Back to overview](index.md)
