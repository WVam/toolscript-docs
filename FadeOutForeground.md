[Back to overview](index.md)

---
# FadeOutForeground (FoutFront)

---

### Description
Fades out the foreground of the screen.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of milliseconds it takes to fade out the foreground.|✓|1000|

### Examples:
#### Example #1: Fading out the foreground over the span of 3 seconds.
```
1:  FadeOutForeground:[3000];
```

#### Example #2: Fading out the foreground over the span of 1 second.
```
1:  FoutFront:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 milliseconds).  
The minimum value for `Duration` is 10. If you use a value lower than 10, it will be considered as 10. The only exception to this is 0, which makes the foreground disappear instantly.

---
[Back to overview](index.md)
