[Back to overview](index.md) • [Back to Investigations article](InvestigationC.md)

---
# Topic

---

### Description
The Instructions in the Talking Container are the topics you can talk about with a character. They are built as in the following scheme:

```
1:  Topic:{DISPLAY TEXT|FIRST INSTRUCTION|SECOND INSTRUCTION|HIDDEN};
```

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|DISPLAY TEXT|String|The text that appears in the button of that topic.|✓|-|
|FIRST PRESENT|Regular Instruction|Executed the first time this topic is chosen.|✓|-|
|SECOND PRESENT|Regular Instruction|Every subsequent time this topic is chosen.|✓|-|
|HIDDEN|Boolean|Determines whether the topic is hidden by default.|✓|-|

### Examples:
#### Example #1: Setting up topic 'Your Alibi'.
```
1:  Topic:{"Your Alibi"|PlayFrame:["LarryAlibi1"]|PlayFrame:["LarryAlibi2"]|false};
```

### Remarks
You can define as many topics per Investigation sequence as you like; however, due to the limited space, only the first 5 topics that aren't hidden will be displayed.

---
[Back to overview](index.md) • [Back to Investigations article](InvestigationC.md)
