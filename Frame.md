[Back to overview](index.md)

---
# Frames

---

Now, Regular Instructions are all fine and dandy, and technically you could use just them. However, you might want to use Frames, especially since they are required for some Instructions.

Now what IS a Frame? A Frame is a Container containing one or more Regular Instructions. It is needed for certain Instructions that require a Frame ID (like [PickEvidence](PickEvidence.md)) or allow the use of a Regular Instruction as a parameter (like some Hybrid Instructions in [Investigations](InvestigationC.md)). You use a Frame when you want to execute multiple Instructions within a single Instruction. Frames are either invoked automatically by Regular Instructions that require a Frame ID or by executing the [PlayFrame](PlayFrame.md) Instruction.
 
And now the most important part:
## How to declare a frame

Frames follow the following syntax:

```
1:  Frame:[ID]<
2:  	-->Insert your Instructions here.<--
3:  >;
```

`ID` is the Frame ID, which allows the Frame to be called by other Instructions.

You can insert the Instructions that are part of the Frame between the Container Brackets (`<>`). Like almost everywhere else, Instructions within Frames must **ALWAYS** end with a semicolon (`;`).

Indentation is not required, but it makes everything look tidier. Don't worry though, we are not Python, we won't kill you if you forget a tabulation somewhere.

## Example:
```
1:  Frame:[0]<
2:  	PlaySound:["GavelSlam"|400];
3:  	LoadScene:["Blackout"|"Judge"|"GavelZoom"|true|true|false];
4:  	PlayMusic:["Trial"];
5:  	LoadScene:["Judge"|"Judge"|"Normal"|false|false|false];
6:  	DisplayText:["Judge"|"Court is now in session for the trial of Mr. Larry Butz."|false|false|false|false];
7:  >;
8:  Frame:["It's the Butz."]<
9:  	LoadScene:["Defense"|"Phoenix"|"Nod"|true|true|false];
10: 	DisplayText:["Phoenix"|"The defense is ready, Your Honor."|false|false|false|false];
11: >;
12: Frame:[3]<
13: 	LoadScene:["Prosecution"|"Miles"|"Bow"|true|true|false];
14: 	DisplayText:["Edgeworth"|"The prosecution is ready as well."|false|false|false|false];
15: >;
16: PlayFrame:["It's the Butz"|3];
```

---
[Back to overview](index.md)
