[Back to overview](index.md)

---
# Branch Instructions
---
Branch Instructions are the loops and conditionals of AACS. They look completely different from other Instructions syntax-wise. They do not follow normal conventions outlined in the rest of the documentation. The unique syntax for Branch Instructions is defined in this article.

## If

The **If** Instruction requires an expression which returns a boolean value. If the boolean value is `true`, then the Instructions within the If statement will be executed. **Else If** and **Else** statements can also be defined in addition to the **If** statement in case the initial expression returns `false`, or a value that isn't a boolean.

Syntax:
```
1:  If [Expression]
2:  (
3:    [AACS HERE]
4:  );
5:  Else If [Expression]
6:  (
7:    [AACS HERE]
8:  );
9:  Else
10: (
11:   [AACS HERE]
12: );
```
>You can learn more about expressions in the documentation about [Variables](Variables.md). **Else** and **Else If** instructions are ignored if the previous instruction is not an **If** or an **Else If**.

## While

The While Instruction takes an expression just like the **If** Instruction. It will then continue to execute the Instructions it contains as long as the expression returns `true`. The loop ceases execution if the expression returns `false` or something that isn't a boolean.

Syntax:
```
1:  Loop While [Expression]
2:  (
3:    [AACS HERE]
4:  );
```

## For

The For Instruction does not take an expression. It requires two parts instead.

Syntax:
```
1:  Loop For [VALUE]: #([COUNTER])
2:  (
3:    [AACS HERE]
4:  );
```
**[VALUE]** can be either a number or a variable which returns a number. If the value or the variable is not a number, the For loop will be skipped like a regular invalid Instruction. Otherwise, the **For** instruction will loop as many times as the **[VALUE]** equals to.

**#([COUNTER])** is a variable which will store the current iteration n-1. This means that the counter equals 0 during the first iteration, 1 during the second iteration, 2 during the third, and so on.

>All Branch Instructions support nesting, meaning that you can put other Branches, or even Containers, inside the brackets of a Branch Instruction.

---
[Back to overview](index.md)
