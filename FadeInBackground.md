[Back to overview](index.md)

---
# FadeInBackground (FinBg)

---

### Description
Fades in the background of the screen.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of milliseconds it takes to fade in the background.|✓|1000|

### Examples:
#### Example #1: Slowly fade in the background over the span of 5 seconds.
```
1:  FadeInBackground:[5000];
```

#### Example #2: Fade in the background with the default duration of 1 second.
```
1:  FinBg:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 milliseconds).  
The minimum value for `Duration` is 10. If you use a value lower than 10, it will be considered as 10. The only exception to this is 0, which makes the background appear instantly.

---
[Back to overview](index.md)
