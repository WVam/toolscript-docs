[Back to overview](index.md)

---
# DecreaseHealth (Damage)

---

### Description
Reduces the amount of health left.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Amount|Number|The amount of health that should be removed.|✓|0|

### Examples:
#### Example #1: Inflicting a penalty of 50 units.
```
1:  ...
2:  DecreaseHealth:[50];
3:  ...
```

#### Example #1: Inflicting a penalty of 20 units.
```
1:  ...
2:  Damage:[20];
3:  ...
```

### Remarks:
The maximum amount of health is 100 units. 
The health bar will automatically be displayed when the health is changed, provided it wasn't already being displayed

Should the health fall to 0 or below, the Frame with the ID `GameOver` will be called, should it exist. Afterwards, the game will end.

---
[Back to overview](index.md)
