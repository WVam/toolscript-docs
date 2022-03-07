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
For example, if this Instruction is called during a press Frame of [Cross Examinations](CrossExamC.md), then the game will end **after** the press Frame has finished executing.

This Instruction will execute the GameOver frame, if it exists.

---
[Back to overview](index.md)
