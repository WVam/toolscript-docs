[Back to overview](index.md)

---
# FadeInScene  (FinScene)

---

### Description
Fades the scene (i.e. character, foreground AND background) back in.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of milliseconds it takes to fade in the scene.|✓|1000|

### Examples:
#### Example #1: Fading in the scene over the span of 2.5 seconds.
```
1:  FadeInScene:[2500];
```

#### Example #2: Fading in the scene over the span of 1 second.
```
1:  FinScene:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 milliseconds).  
The minimum value for `Duration` is 10. If you use a value lower than 10, it will be considered as 10. The only exception to this is 0, which makes the scene appear instantly.

---
[Back to overview](index.md)
