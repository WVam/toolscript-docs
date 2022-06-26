[Back to overview](index.md)

---
# SelectSpot (Spot)

---

### Description
Prompts the player to select a point on the screen.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|X Pos|String|The position of the correct spot on the x-axis.|✓|-|
|Y Pos|Number|The position of the correct spot on the y-axis.|✓|-|
|Offset|Boolean|The offset around the x and y positions (by how much the x and y positions of the clicked spot can differ from `X Pos` and `Y Pos` respectively while still be considered correct).|✓|-|
|Correct Frame|Boolean|The ID of the frame that should be played when the correct spot is clicked.|✓|-|
|Wrong Frame|Boolean|The ID of the frame that should be played when the wrong spot is clicked.|✓|-|

### Examples:
#### Example #1: Prompt the player to click a spot on (20,30) with an offset of 10 pixels. If the player clicks on that spot, frame '2' will be played. Otherwise frame '3' will be played.
```
1:  SelectSpot:[20|30|10|2|3];
```

### Remarks:
You can omit all parameters (`SelectSpot:[-];`) if you don't want to check for any specific coordinates. The player will still be prompted to select a point on the screen, but no frame will be executed. Instead, the selected coordinates will be stored in 2 variables:
- **Sys_SelectedPointX**: The position on the X axis of the selected point.
- **Sys_SelectedPointY**: The position on the Y axis of the selected point.

---
[Back to overview](index.md)
