[Back to overview](index.md)

---
# Variables

---

Variables, like all Instructions, have a set syntax. They have the following format: #([VARNAME]).  
[VARNAME] can be any alphanumerical string (a-z, A-Z, 0-9).

Variables can have 4 different types: **String**, **Boolean**, **Number**, and **Undefined**. Keep in mind, variables are not strong typed. This means that the type can change at any time. The type is set implicit depending on the value it receives.

## Quick Overview:

* [](#)**String**
>A string is simple text. Encapsulating the value in quotes ("") will turn the variable into a string-type variable.  
>A string has the second highest priority.


<<<<<<< HEAD
* [](#)**Number**
>Numbers are whole numbers. This means that numbers have the range of a 32-bit integer with decimals not allowed.  
>A number has the third highest priority.

* [](#)**Boolean**
>A boolean has two values: True and False (not case sensitive). Booleans are used for the If and While branch instructions. An expression must always return a boolean when used in a branch instruction, or else the branch instruction will be ignored. Branches can be studied in their appropriate article.  
>Booleans have the lowest (fourth highest) priority.

* [](#)**Undefined**
>If a variable has no value defined, its type will be undefined. This can happen in two ways: if you access a variable that was never defined, in which case it will be initialized with no value, or if you explicitly set the value to undefined by using the **Null** keyword.  
>This type has the highest priority.

## Combining Variables
As mentioned earlier, the different variable types have priorities. These priorities come into play when combining variables with different types. Combining includes the operations: addition, subtraction, multiplication, division, greater than, less than, equal, and not equal. Combinations marked with an X will always result in an empty value and an Undefined variable type. Some operations do not make mathematical sense or are even possible, and will result in an Undefined variable type. Others are mapped to special operations.

### Addition (+)

|+|**String**|**Number**|**Boolean**|**Undefined**|
|:-:|:-:|:-:|:-:|:-:|
|**String**|String|String|String|String|
|**Number**|String|Number|Number|X|
|**Boolean**|String|Number|Boolean|X|
|**Undefined**|String|X|X|X|

#### Effects
>**String ⟷ String**: The two strings will be joined together into a single string. The second string will be appended to the first string.  
>**String ⟷ Number**: The number will be considered as a string and the two values will be joined together into a single string. The second value will be appended to the first value.  
>**String ⟷ Boolean**: The boolean will be considered as a string (True = "true", False = "false") and the two values will be joined together into a single string. The second value will be appended to the first value.  
>**String ⟷ Undefined**: The undefined value will be considered as the string "null" and the two values will be joined together into a single string. The second value will be appended to the first value.    
>**Number ⟷ Number**: The two numbers will be added together.  
>**Number ⟷ Boolean**: The boolean will be considered as a number (True = 1, False = 0) and the two values will be added together.  
>**Boolean ⟷ Boolean**: An AND operation will be performed between the two booleans. This operation returns True if both booleans equal True, and False otherwise.

### Subtraction (-)

|-|String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|**String**|String|String |String |String|
|**Number**|String|Number |Number |X|
|**Boolean**|String|Number|Boolean|X|
|**Undefined**|String|X|X|X|

#### Effects
>**String ⟷ String**: Every occurence of the second string will be removed from the first one.  
>**String ⟷ Number**: The number will be considered as a string and every occurence of the second value will be removed from the first value.  
>**String ⟷ Boolean**: The boolean will be considered as a string (True = "true", False = "false") and every occurence of the second value will be removed from the first value.  
>**String ⟷ Undefined**: The undefined value will be considered as the string "null" and every occurence of the second value will be removed from the first value.  
>**Number ⟷ Number**: The second number will be subtracted from the first number.  
>**Number ⟷ Boolean**: The boolean will be considered as a number (True = 1, False = 0) and the second value will be subtracted from the first value.  
>**Boolean ⟷ Boolean**: An OR operation will be performed between the two booleans. This operation returns False if both booleans equal False, and True otherwise.


### Multiplication (\*)

|\*|**String**|**Number**|**Boolean**|**Undefined**|
|:-:|:-:|:-:|:-:|:-:|
|**String**|Boolean|Boolean|Boolean|Boolean|
|**Number**|Boolean|Number|X|X|
|**Boolean**|Boolean|X|Boolean|X|
|**Undefined**|Boolean|X|X|X|

#### Effects
>**String ⟷ String**: Returns True if the first string starts with the second string, and False otherwise.  
>**String ⟷ Number**: The number will be considered as a string. Returns True if the first value starts with the second value, and False otherwise.  
>**String ⟷ Number**: The boolean will be considered as a string (True = "true", False = "false"). Returns True if the first value starts with the second value, and False otherwise.  
>**Number ⟷ Number**: The undefined value will be considered as the string "null". Returns True if the first value starts with the second value.  
>**Boolean ⟷ Boolean**: An XOR operation will be performed between the two booleans. This operation returns True if the two values are not equal to each other, and False otherwise.

### Division (/)

|/|**String**|**Number**|**Boolean**|**Undefined**|
|:-:|:-:|:-:|:-:|:-:|
|**String**|Boolean|Boolean|Boolean|Boolean|
|**Number**|Boolean|Number|X|X|
|**Boolean**|Boolean|X|X|X|
|**Undefined**|Boolean|X|X|X|

#### Effects
>**String ⟷ String**: Returns True if the first string ends with the second string, and False otherwise.  
>**String ⟷ Number**: The number will be considered as a string. Returns True if the first value ends with the second value, and False otherwise.  
>**String ⟷ Boolean**: The boolean will be considered as a string (True = "true", False = "false"). Returns True if the first value ends with the second value, and False otherwise.  
>**String ⟷ Undefined**: The undefined value will be considered as the string "null". Returns True if the first value ends with the second value.  
>**Number ⟷ Number**: The first number will be divided by the second number. 

### Greater Than/Less Than (<\|>)

|<, >|**String**|**Number**|**Boolean**|**Undefined**|
|:-:|:-:|:-:|:-:|:-:|
|**String**|Boolean|Boolean|Boolean|Boolean|
|**Number**|Boolean|Boolean|Boolean|X|
|**Boolean**|Boolean|Boolean|X|X|
|**Undefined**|Boolean|X|X|X|

#### Effects
>**String ⟷ String**: Returns True if the first string is longer/shorter than the second string, and False otherwise.  
>**String ⟷ Number**: The number will be considered as a string (True = "true", False = "false"). Returns True if the first string is longer/shorter than the second string, and False otherwise.  
>**String ⟷ Boolean**: The boolean will be considered as a string. Returns True if the first string is longer/shorter than the second string, and False otherwise.  
>**String ⟷ Undefined**: The undefined value will be considered as the string "null". Returns True if the first string is longer/shorter than the second string, and False otherwise.  
>**Number ⟷ Number**: Returns True if the first number is greater/less than the second number, and False otherwise  
>**Boolean ⟷ Boolean**: Checks if the first boolean is greater than 0.

### Equal/Not Equal (=\|!=)

|=, !=|**String**|**Number**|**Boolean**|**Undefined**|
|:-:|:-:|:-:|:-:|:-:|
|**String**|Boolean|Boolean|Boolean|Boolean|
|**Number**|Boolean|Boolean|Boolean|X|
|**Boolean**|Boolean|Boolean|Boolean|X|
|**Undefined**|Boolean|X|X|Boolean|

#### Effects
>**String ⟷ String**: Returns True if the two strings are equal, and False otherwise.  
>**String ⟷ Number**: The number will be considered as a string. Returns True if the two strings are equal, and False otherwise.  
>**String ⟷ Boolean**: The boolean will be considered as a string (True = "true", False = "false"). Returns True if the two strings are equal, and False otherwise.  
>**String ⟷ Undefined**: The undefined value will be considered as the string "null". Returns True if the two strings are equal, and False otherwise.  
>**Number ⟷ Number**: Returns True if the two numbers are equal, and False otherwise.  
>**Number ⟷ Boolean**: The boolean will be considered as a number (True = 1, False = 0). Returns True if the two numbers are equal, and False otherwise.  
>**Boolean ⟷ Boolean**: Returns True if the two booleans are equal, and False otherwise.  
>**Undefined ⟷ Undefined**: Returns True if the two undefined values are equal, and False otherwise.

## Expressions & Additional Information
It is important to know that strings will always consider the second value as a string as well. This means that the string "40" **DOES** equal the number 40, for example.  
But "80" is not greater than 40; They're both strings with 2 characters.

### Expressions:  
The combinations mentioned above come into play when using expressions.  
An expression is nothing but a chain of variable commands. An expression is either a single value/variable or multiple values and/or variables with an operator between each of them.  
You can chain as many variables and operators together as you need.

A variable can be set with the following Instruction:
```
1: Set #([VARNAME]) = [EXPRESSION];
```
Where [EXPRESSION] can be something like:
```
#(MyVar) + 4 * 3 / 2 - #(Var2)
```

Keep in mind that, since mathematics are very unlikely to be used in AACT, the brackets ( and ) are not supported.

Like Branch Instructions, this will be executed like a Regular Instruction, even though it does not follow the regular syntax.  
Be mindful of typos while creating expressions, as these can result in undefined values being returned unexpectedly.

---
[Back to overview](index.md)
