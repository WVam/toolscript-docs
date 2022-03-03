[Back to overview](index.md)

---
# CrossExamination

---
The CrossExamination Instruction is obviously used for processing a Cross-examination. The way this Container is defined is similar to the way a Frame is defined:

```
1:  CrossExamination:[ID|MODE]<
2:     ->INSTRUCTIONS<-
3:  >;
```
**MODE** refers to how the Cross-examination can be finished. If set to 1, the Cross-examination will only end if the player has pressed all statements at least once.
Every other number means a contradiction has to be found.
> If you want to combine it, meaning you want the Cross-examination to end either way, set it to 1. That will take care of the "Press" condition. And to end it by objecting, execute the [FinishCrossExam](FinishCrossExam.md) Instruction in a Frame that gets executed through the PickEvidence Instruction mentioned below.  

A Cross-examination, just like Frames, is a Container Instruction, which means it can host multiple Instructions inside. Unlike Frames, however, you are limited as to what kind of Instructions you can add to the body of the Cross-examination.

## Statements

In a Cross-examination, you only can use Statement Instructions. Like Cross-examinations, Statement Instructions are Container Instructions, hence they use the Container brackets "<" and ">". Also, just like the CrossExamination Instruction, they are also limited. But unlike Statement Instructions, these are limited by the umber of Instructions they can contain. They only allow two plus one optional Regular Instruction. Any more or any less and the script will fail to load. 

A Statement Instruction is built like this:

```
1:  SNUM:<Instruction1;Instruction2;Instruction3;>
```

> Statement Instructions do NOT end with a semicolon.
 
**NUM** is the number of the statement Instruction. The first one must always be "1". The upper limit is 10, so you can have a maximum of 10 statements per Cross-examination.

Now, Instruction 1, 2, and 3 can be any Regular Instruction you want. But it only makes sense for them to be two kinds of Instruction.

Instruction 1 and 2 should be a [PlayFrame](PlayFrame.md) Instruction. Instruction 1 will be executed when the Statement is being played (so it should contain a [PlayFrame](PlayFrame.md) Instruction that plays a Frame that displays green text). Instruction 2 will be executed when the player clicks on the "Press" button.  
Instruction 3 is optional. But if you use it, it **must** be a [PickEvidence](PickEvidence.md) Instruction. Add this to the statement that contains a contradiction to make it objectionable.

> Attention: Currently there can only be one statement marked as "contradiction" per Cross-examination. If you add the PickEvidence to multiple statements, only the first one will be considered.

## Special Statements

Then there are two other Statement Instructions. They don't actually have anything to do with a statement, however.
These are called SCO and SEV and each of them only allows a single Regular Instruction, which, again, should be a [PlayFrame](PlayFrame.md) Instruction.
The SCO will be executed after the last statement has been displayed. You should use it for discussions with the counsel like in the games which usually gives a vague hint on where to look for clues.
The SEV will be executed when the player objects (presses "Present") in a statement that doesn't have a contradiction. 

An example Cross-examination could look like this:

```
1:  CrossExamination:[0|1]<
2:     S1:<Frame[1];Frame[5];>   
3:     S2:<Frame[2];Frame[6];PickEvidence:["Autopsy report"|1|11|10];>
4:     S3:<Frame[3];Frame[7];>
5:     S4:<Frame[4];Frame[8];>
6:     SCO:<Frame[9];>
7:     SEV:<Frame[10];>
8:  >;
``` 

>While you can [hide](HideStatement.md) and [reveal](RevealStatement.md) statements of a Cross-examination, you can't set an initial state. Initially, all statements are revealed by default.  
This is because this feature was forgotten when Cross-examinations were implemented, and I'm too lazy to adjust the script parser for this. Oh well.

---
[Back to overview](index.md)
