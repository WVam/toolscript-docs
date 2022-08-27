[Back to overview](index.md)

---
# Basics

---
Before getting into the Instructions of the **Ace Attorney Casing Tool Script (AACS)**, there is some information and terminology that you ought to know.

1. AACS is very forgiving. If you make typos or pass the wrong parameters, the game won't usually crash: instead, the erroneous lines will be skipped and the next Instruction will be read.
    
    The exact reason for an Instruction to be ignored can be any of the following:
    1. The Instruction starts with `->`, which indicates that this and any subsequent lines until `<-` are comments.
    2. The Instruction cannot be interpeted. Normally caused by a typo or syntax error.
    3. There are not enough parameters, or they cannot be interpreted. Some Instructions require parameters: too few and the Instruction will be ignored, too many and the superfluous parameters will be ignored. Occasionally, the engine might crash if it fails to interpret a parameter.

2. **Instructions** are the actual commands for the game that you can write in the script. There are four types of Instructions: **Regular Instructions**, **Container Instructions**, **Hybrid Instructions** and **Branch Instructions**.

    **Regular Instructions** are the common Instructions for actual actions that are displayed on screen like changing scenes, displaying popups, presenting evidence, or showing dialogue.
 
    **Container Instructions** work a bit differently. They contain multiple Regular Instructions. Container Instructions also have an individual ID assigned to each of them. The reason for that is simple: a Container Instruction has to be explicitly called via a Regular Instruction. A Regular Instruction is executed as soon as the engine reads the line. A Container Instructions won't be executed when it is read. This allows you, for example, to prepare Cross Examinations or Frames that are used more than once at the top of the script file. As of now, there are three Container Instructions, which are explained in their respective pages.
 
    **Hybrid Instructions** are a mix between Regular Instructions and Container Instructions. In a Hybrid Instruction you can pass parameters like in a Regular Instruction. However, unlike Regular Instructions, a parameter in a Hybrid Instruction can be either a value or a Regular Instruction. Currently, Hybrid Instructions only appear in Investigations and Mood Matrix sequences.

    **Branch Instructions** are conditional branches (If and Else) and loops (For and While).

3. Most Instruction parameters are optional, which means that you don't have to type them at all. If all parameters of an Instruction are optional, and you decide not to use any of them, you can use a dash `-` character instead (i.e. [`FadeOutScene:[-];`](FadeOutScene.md)). Now, be aware that, in this case, you MUST use this syntax. You cannot simply leave the Instruction brackets out (i.e. `FadeOutScene;`). This syntax is reserved for Instructions that don't have parameters to begin with, like the [Break](Break.md) Instruction. 

	Additionally, you must enter all parameters that come before the one you want to use. This means that, if you want to use the third parameter of an Instruction, you must enter the first and second parameter as well. You can, however, use the null character (-) for them in order to indicate that you want to use the default value.

## Syntax

There are 9 important syntax elements in AACS.
1. **The semicolon**  
    Semicolons are used to indicate the end of an Instruction. They are required at the end of almost every Instruction, save for a select few. If there is no semicolon at the end of an Instruction, the engine will skip the line and not execute the Instruction (see 6. **Comments** for more info).
    
2. **The Instruction header**  
	All Instructions except Branch Instructions follow the same syntax.
	```
	INSTRUCTIONNAME:[PARAMETERS]
	```
	It is important not to have any whitespace between the name and the colon or between the colon and the parameters.

3. **The parameter brackets `[]`**  
	The parameter brackets are used to define the space for parameters in Instructions. Single parameters are split using the pipe "\|" symbol.

4. **The Instruction brackets `<>`**  
	The Instruction brackets are used for (and inside) Container Instructions to contain the Regular Instructions. They are also used for statements in Cross Examinations.

5. **The hybrid brackets `{}`**  
	Within these brackets are parameters which may be either values or Regular Instructions. Single parameters are split using the pipe "\|" symbol, like in Regular Instructions.

6. **Comments `-> <-`**  
	Comments are used to force the engine to ignore certain segments of script, or to write notes about the script.  
	
	> Technically, you are not required to use this syntax for comments, as the engine will not parse any text it cannot understand as an Instruction; however, not using this syntax can lead to unexpected issues.  
	>   
	> For example, you may have two lines in the script editor:
	> ```
	> 1: This line is a comment, but it doesn't use the comment syntax.
	> 2: LoadScene:["Defense"|"Phoenix"|false|false];
	> ```
	> The result of running these two lines of script is that neither line is executed. The engine does not read whitespace characters like line breaks, and this script is interepreted like this:
	> ```
	> 1: This line is a comment, but it doesn't use the comment syntax.LoadScene:["Defense"|"Phoenix"|false|false];
	> ```
	> This is not a valid Instruction, so all of it is skipped.
	>  
	> However, were it properly stylized as a comment (i.e. encapsulated in `->` and `<-`), it would be interpreted like this:
	> ```
	> 1: LoadScene:["Defense"|"Phoenix"|false|false];
	> ```
	> Comments are removed during compilation so only the valid Instruction is left.

7. **Null character `-`**  
	AACS uses a dash `-` to represent the absence of a value. If this is used instead of a parameter, the default value for that parameter will be used.  
	> This can greatly change the behaviour of some Instructions. For instance, passing `-` to the ```Character name``` parameter of the [DisplayText](DisplayText.md) Instruction hides the name box, and passing `-` to certain parameters of the [ButtonChoice](ButtonChoice.md) Instruction changes the number of buttons to be displayed.

8. **Variables**  
	Variables are written like this:
	```
	1: #(VARIABLENAME) 
	```
	And you can set them like this:
	```
	1: Set #(VARIABLENAME) = EXPRESSION
	```
	Keep in mind that variables behave like Regular Instructions, but have their own syntax. For more information on variables and expressions, read the [Variables](Variables.md) page.

9. **Branch Instructions**  
	Branch Instructions are declared using the following syntax (although Else and For deviate from this slightly):
	```
	1: INSTRUCTIONNAME #(VARIABLE) = EXPRESSION
	2: (
	3:   ->Your AACS here<-
	4: ); 
	```
	For more information on Branch Instructions, read the [Branch Instructions](Branch-Instructions.md) page.

---
[Back to overview](index.md)
