[Back to overview](index.md)

---
# FadeOutCharacter (FoutChar)

---

### Description
Fades out a character.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Delay|Number|The amount of milliseconds it takes to fade out the character.|✓|1000|
|Position|String|The name of the position used in [LoadCharacter](LoadCharacter.md). Used to identify the character.|✗|"Center"|

### Examples:
#### Example #1: Fade out the character of the 'Center' position over the span of 3 seconds.
```
1:  FadeOutCharacter:[3000];
```

#### Example #2: Fade out the character of the 'Center' position over the span of 1 second.
```
2:  FoutChar:[-];
```

#### Example #3: Fade out the character of the 'Left' position over the span of 1.5 seconds.
```
3:  FadeOutCharacter:[1500|"Left"];
```

#### Example #4: Fade out the character of the 'Right' position over the span of 1 second.
```
4:  FoutChar:[-|"Right"];
```

### Remarks:
If you pass an empty parameter as `Delay`, it will default to one second (1000 milliseconds).  
The minimum value for `Delay` is 10. If you use a value lower than 10, it will be considered as 10. The only exception to this is 0, which makes the character disappear instantly.

---
[Back to overview](index.md)
