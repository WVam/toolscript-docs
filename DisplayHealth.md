[Back to overview](index.md)

---
# DisplayHealth (DH)

---

### Description
Displays the health bar in the top right corner.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Slide|Boolean|Whether the health bar should slide into view or appear instantly.|✗|false|

### Examples:
#### Example #1: Display the health bar with a sliding animation.
```
1:  DisplayHealth:[true];
```

#### Example #1: Display the health bar instantly.
```
1:  DH:[false];
```

### Remarks:
Do not confuse the health bar with the psyche bar: the first is the regular health bar that is usually displayed during a trial, while the second one is for Psyche Lock sequences. The health bar is on the left side, as opposed to the psyche bar which is on the right side.

There is a special frame ID `GameOver` which you can give to a frame to mark it as a GameOver frame. A GameOver frame will be called if the health drops down to 0. Once the contents of the GameOver frame have been executed, the game will automatically end.

The appearance and position of the health bar can be modified via Themes.

---
[Back to overview](index.md)
