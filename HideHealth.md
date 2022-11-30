[Back to overview](index.md)

---
# HideHealth (HH)

---

### Description
This Instruction hides the health bar.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Mode|Boolean|Determines whether or not a sliding animation should be used.|✓|false|

### Examples:
#### Example #1: Hide the health bar with a sliding animation.
```
1:  HideHealth:[true];
```

#### Example #2: Hide the health bar without a sliding animation.
```
1:  HH:[false];
```

### Remarks:
Do not confuse the health bar with the psyche bar: the first is the regular health bar that is usually displayed during a trial, while the second one is for Psyche Lock sequences. The health bar is on the left side of the screen, as opposed to the psyche bar which is on the right side.

There is a special frame ID `GameOver` which you can give to a frame to mark it as a GameOver frame. A GameOver frame will be called if the health drops down to 0. Once the contents of the GameOver frame have been executed, the game will automatically end.

The appearance and position of the health bar can be modified via Themes.

---
[Back to overview](index.md)
