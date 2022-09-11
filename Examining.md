[Back to overview](index.md) • [Back to Investigations page](InvestigationC.md)

---
# Examining

---

Examining is the most complex part of an [Investigation](InvestigationC.md) sequence. An Examining Container features 4 different Hybrid Instructions: AllExamined, AlreadyExamined, PointDefault and Point.

## AllExamined
This Hybrid Instruction contains one parameter which is a Regular Instruction. It will be executed once the player has examined all the spots, which are defined by a Point Instruction.

Example:
```
1:  AllExamined:{PlayFrame:[1]};
```

## AlreadyExamined
This Hybrid Instruction contains one parameter which is a Regular Instruction. It will be executed when the player clicks on the "Examine" button after having examined all spots, which are defined by a Point Instruction.

Example:
```
1:  AlreadyExamined:{PlayFrame:[2]};
``` 

## PointDefault
This hybrid instruction contains one parameter which is a Regular Instruction. It will be executed when the player examines a spot on the upper screen that is not defined by a Point Instruction.

Example:
```
1:  PointDefault:{PlayFrame:[3]};
``` 

## Point
This is the main part of an examination. A point is a spot on the upper screen on which the player has to click in order to invoke some action. The Point Instruction is built using the following scheme:
```
Point:{X|Y|OFFSET|FIRST DISCOVER|SECOND DISCOVER};
```

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|X|Number|The position of the point on the x-axis.|✓|-|
|Y|Number|The position of the point on the y-axis.|✓|-|
|OFFSET|Number|The offset around the X and Y positions (by how much the x and y positions of the clicked spot can differ from `X` and `Y` respectively while still being considered part of the point).|✓|-|
|FIRST DISCOVER|Regular Instruction|Gets executed the first time that the player clicks on this point.|✓|-|
|SECOND DISCOVER|Regular Instruction|Gets executed every subsequent time that the player clicks on this point.|✓|-|

Example:
```
1:  Point:{24|48|10|PlayFrame:["DiscoverKnife"]|PlayFrame:["RediscoverKnife]};
``` 

There can be as many Point Instructions as you want.

---
[Back to overview](index.md) • [Back to Investigations page](InvestigationC.md)
