[Back to overview](index.md)

---
# Mood Matrix

---

The Mood Matrix (or MM) is a gameplay mechanic introduced in Phoenix Wright™: Ace Attorney™ – Dual Destinies. It allows the user to visualize a person's true emotions.

The goal is to point out contradicting emotions when compared with the person's spoken testimony. For example, if a witness claims they were angry about something, but the Mood Matrix shows that the witness is feeling happiness, you can deduce something is wrong.

In AACT, a Mood Matrix works almost the same as a [Cross Examination](CrossExamC.md) save for some minor differences.

Example:
```
1:  MoodMatrix:["AngryMaya"]<
2:  S1:{PlayFrame:[0]|"Happy"|PlayFrame:["ThisFrame"]}
3:  S2:{PlayFrame:[0]}
4:  SCO:<PlayFrame:["ThatFrame"];>
5:  SMF:<PlayFrame:[0];>
6:  >;
```

Unlike the [CrossExamination](CrossExamC.md) Instruction, the MoodMatrix Instruction does not have a MODE parameter.

## Statements
Statements in Mood Matrices (SNUM) also have the same purpose as Statements in Cross Examinations, but they work a bit differently.
In the Mood Matrix syntax, the Statement Instructions are Hybrid Instructions, not Container Instructions. This means that they work like Regular Instructions with the difference that they allow Regular Instructions (as well as values) to be passed as parameters. Despite this, of course, they still have a set order.
The first parameter is the Instruction that is played as the statement. Here you will probably want to play a frame that makes the character talk and makes emojis stop or start pulsating depending on the character's emotions.
The second and third parameter are optional.
The second parameter determines a contradicting emotion. If the player pinpoints this emotion, the third parameter is executed.
Afterwards, just like a successful "presenting" ends a Cross Examination, a successful poinpointing ends a Mood Matrix sequence.

## Special Statements
SCO and SMF are the same as SCO and SEV in Cross Examinations. The only difference is that in a Cross Examination, SEV is played when a wrong piece of evidence was presented, whereas in a Mood Matrix sequence, the SMF is played when the wrong emotion was pinpointed.

---
[Back to overview](index.md)
