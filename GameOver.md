[Back to overview](index.md)

---
# GameOver

---
### Description
Requests that the game end.

### Parameters
This Instruction has no parameters.

### Examples:
#### Example #1: Request a Game Over.
```
1:  GameOver;
```

### Remarks:
If this Instruction is called, the game will not end immediately. Usually, the engine will wait for a dialog to finish first.
For example, if this Instruction is called during the Frame of a [Cross Examination](CrossExamC.md) that plays after pressing the "Press" button, then the game will end **after** the Frame has finished executing.

This Instruction will execute the GameOver Frame, if it exists.

---
[Back to overview](index.md)
