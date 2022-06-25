[Back to overview](index.md)

---
# Move

---

 ### Description:
Moving describes the action that would correspond to switching locations in the game. The Move Instructions are Hybrid Instructions, meaning their parameters can be values or Regular Instructions. A Move Instruction is construced with the following scheme:

```
1:  Move:{DISPLAY TEXT|INSTRUCTION|HIDDEN};
```
### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|DISPLAY TEXT|String|The text that will appear on the button in the moving menu.|
|INSTRUCTION|Regular Instruction|The Regular Instruction that will be executed when clicking on the movement option.|
|HIDDEN|Boolean|Determines whether or not the moving option is hidden by default.|

### Examples:
#### Example #1: Setting up the moving option to move to another investigation.
```
1: Move:{"Wright Anything Agency"|PlayInvestigation:["Agency"]|false};
```

### Remarks:
You can define as many Move Instructions as you like per Investigation sequence, however only the first 4 Move Instructions that are not hidden will be shown.

---
[Back to overview](index.md)
