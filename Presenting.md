[Back to overview](index.md) • [Back to Investigations article](InvestigationC.md)

---
# Presenting
---

### Description:
Presenting refers to the action of showing a person a piece of evidence outside of court in order to elicit dialogue or progress the story. There are 4 different types of presenting: Evidence, Profile, DefaultEvidence and DefaultProfile. For each piece of evidence you want to be presented you use Evidence, and for each profile you want to be presented you use Profile. All other pieces of evidence or profiles are covered by the DefaultEvidence and DefaultProfile Instructions, which will be executed when a piece or profile is shown that isn't covered by an Evidence or Profile Instruction (e.g. irrelevant evidence and profiles).
An Instruction in the Presenting Container is built as in the following scheme:
```
1:  TYPE:{NAME|FIRST PRESENT|SECOND PRESENT};
```

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|TYPE|Record|Can be either "Evidence" or "Profile".|✓|-|
|NAME|String|The name of the evidence or the profile that can be presented.|✓|-|
|FIRST PRESENT|Regular Instruction|Executed the first time this record is presented.|✓|-|
|SECOND PRESENT|Regular Instruction|Every subsequent time this record is presented.|✓|-|

### Examples:
#### Example #1: Defines which Instructions to execute when the evidence "Attorney's Badge" is presented. The first time it is presented, frame '12' will be executed. If it is presented again after the first time, frame '13' will be executed.
```
1:  Evidence:{"Attorney's Badge"|PlayFrame:[12]|PlayFrame:[13]};
```

#### Example #2: Defines which Instructions to execute when the profile "Attorney's Badge" is presented. The first time it is presented, frame '14' will be executed. If it is presented again after the first time, frame '15' will be executed.
```
1:  Profile:{"Blue Badger"|PlayFrame:[14]|PlayFrame:[15]};
```

### Remarks
TYPE can also be "DefaultEvidence" or "DefaultProfile". However, in that case the hybrid only has one parameter: a Regular Instruction that is executed when a piece of evidence or a profile that is not covered by another Present Instruction is presented. You can define as many DefaultEvidence or DefaultProfile Instructions as you want, but only the first one of each will be used.
Example: 

```
1:  DefaultEvidence:{PlayFrame:[16]};
2:  DefaultProfile:{PlayFrame:[17]};
```

---
[Back to overview](index.md) • [Back to Investigations article](InvestigationC.md)
