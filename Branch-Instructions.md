[Back to overview](index.md)

---
# Branch Instructions

---

Branch Instructions are the loops and conditionals of AACS. They look completely different from other Instructions syntax-wise. They do not follow normal conventions outlined in the rest of the documentation. The unique syntax for Branch Instructions is defined in this article.

## If

The **If** Instruction requires an expression which returns a boolean value. If the boolean value is True, then the Instructions within the **If** statement will be executed. **Else If** and **Else** statements can also be defined in addition to the **If** statement in case the initial expression returns False, or a value that isn't a boolean.

Syntax:
```
1:  If [Expression]
2:  (
3:    -> The Instructions contained here are executed
         if [Expression] returns True <-
4:  );
5:  Else If [Expression2]
6:  (
7:    -> The Instructions contained here are executed
         if [Expression] does NOT return True
         AND [Expression2] returns True <-
8:  );
9:  Else
10: (
11:   -> The Instructions contained here are executed
         if [Expression] does NOT return True
         AND [Expression2] does NOT return True <-
12: );
```
>You can learn more about expressions in the documentation about [Variables](Variables.md). **Else** and **Else If** Instructions are ignored if the previous Instruction is not an **If** or an **Else If**.

## While

The **While** Instruction takes an expression just like the **If** Instruction. It will then continue to execute the Instructions it contains as long as the expression returns True. The loop stops being executed if, at the end of a loop, the expression returns False or something that isn't a boolean.

Syntax:
```
1:  Loop While [Expression]
2:  (
3:    ->Your AACS here<-
4:  );
```

## For

The **For** Instruction does not take an expression. It requires two parts instead.

Syntax:
```
1:  Loop For [VALUE]: #([COUNTER])
2:  (
3:    ->Your AACS here<-
4:  );
```
**[VALUE]** can be either a positive number or a variable which returns a positive number. If the value or the variable is not a positive number, the **For** loop will be skipped like a regular invalid Instruction. Otherwise, the **For** Instruction will loop as many times as the **[VALUE]** equals to.

**#([COUNTER])** is a variable which will store the current iteration n-1. This means that the counter equals 0 during the first iteration, 1 during the second iteration, 2 during the third, and so on.

> All Branch Instructions support nesting, meaning that you can put other Branches, or even Containers, inside the brackets of a Branch Instruction.

---
[Back to overview](index.md)
