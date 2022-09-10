[Back to overview](index.md)

---
# CrossExamination (CrossExam, CE)

---

The CrossExamination Instruction, as the name implies, is used for processing a Cross Examination. The way this Container is defined is similar to the way a [Frame](Frame.md) is defined:

```
1:  CrossExamination:[ID|MODE]<
2:     ->INSTRUCTIONS<-
3:  >;
```

`MODE` refers to how the Cross Examination can be finished. If set to 1, the Cross Examination will only end if the player has pressed all Statements at least once.
Any other number means that a contradiction has to be found in order for the Cross Examination to be finished.
> Regardless of the `MODE`, you can always end a Cross Examination by using the [FinishCrossExam](FinishCrossExam.md) Instruction.
> If you want to combine the two modes, meaning you want the Cross Examination to end either way, set it to 1. That will take care of the "Press" condition. To end it by objecting, execute the FinishCrossExam Instruction in a Frame that gets executed through the PickEvidence Instruction mentioned below.  

Cross Examinations, just like Frames, are Container Instructions, which means they can host multiple Instructions inside. Unlike Frames, however, you are limited as to what kind of Instructions you can add to the body of the Cross Examination.

## Statements

In a Cross Examination, you can only use Statement Instructions. Like Cross Examinations, Statement Instructions are Container Instructions, hence they use the Container brackets `<` and `>`.

Just like the CrossExamination Instruction, Statement Instructions are limited. However, unlike CrossExamination Instructions, these are limited as to the number of Instructions they can contain. They only allow two required Regular Instructions plus an optional one. Any more or any less and the script will fail to load. 

A Statement Instruction is built like this:

```
1:  SNUM:<Instruction1;Instruction2;Instruction3;>
```

> Statement Instructions do **NOT** end with a semicolon.
 
**NUM** is the number of the Atatement Instruction. The first one must always be "1". The upper limit is 10, so you can have a maximum of 10 Statements per Cross Examination.

`Instruction1` and `Instruction2` can be any Regular Instruction you want, but it only makes sense for them to be [PlayFrame](PlayFrame.md) Instructions. `Instruction1` will be executed when the Statement is being played (so it should contain a [PlayFrame](PlayFrame.md) Instruction that plays a Frame that displays green text). `Instruction2` will be executed when the player clicks on the "Press" button.  

`Instruction3` is optional, but if you use it, it **must** be a [PickEvidence](PickEvidence.md) Instruction. Add this to the Statement that contains a contradiction to make it objectionable.

> Attention: Currently there can only be one Statement marked as "objectionable" per Cross Examination. If you add the [PickEvidence](PickEvidence.md) to multiple Statements, only the first one will be considered.

## Special Statements

Then there are two other Statement Instructions which are not actually Statements.
These are called SCO and SEV and each of them only allows a single Regular Instruction. As with `Instruction1` and `Instruction2`, this can be any Regular Instruction, but it only makes sense for it to be a [PlayFrame](PlayFrame.md) Instruction.
The SCO will be executed after the last Statement has been displayed. You should use it for discussions with the co-counsel like in the games which usually gives a vague hint on where to look for clues.
The SEV will be executed when the player objects (presses "Present") in a Statement that doesn't have a contradiction. 

## Example

Here is an example CrossExamination Instruction:

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

## Remarks

While you can [hide](HideStatement.md) and [reveal](RevealStatement.md) the Statements in a Cross Examination, you can't set an initial state. Initially, all Statements are revealed by default.  
> This is because this feature was forgotten when Cross Examinations were originally implemented, and I'm too lazy to adjust the script parser for this. Oh well.

---
[Back to overview](index.md)
