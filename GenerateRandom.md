[Back to overview](index.md)

---
# GenerateRandom (RNG)

---

### Description
Randomizes the value of a variable according to its type. If the specified variable doesn't exist, a new one will be created.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Variable name|String|The name of the variable the value of which should be randomized.|✓|-|
|Number 1|Number|A number used by the Instruction. See [Remarks](#remarks).|✓|0|
|Number 2|Number|A number used by the Instruction. See [Remarks](#remarks).|✗|20|

### Examples:
#### Example #1: Setting the variable #(MyVar) to a random Number value between 20 and 30 inclusive. If the variable doesn't exist, it will be created.
```
1:  GenerateRandom:["MyVar"|20|30];
```

#### Example #2: Setting the variable #(MyVar) to a random Number value between 20 and 30 inclusive.
```
1:  Set #(MyVar) = 0;
2:  GenerateRandom:["MyVar"|280];
```

#### Example #3: Setting the variable #(MyStringVar) to a random String value that is 30 characters long. If the variable doesn't exist, it will be created.
```
1:  GenerateRandom:["MyStringVar"|30];
```

#### Example #4: Setting the variable #(MyBooleanVar) to a random Boolean value, giving it a 25% chance of being True.
```
1:  Set #(MyBooleanVar) = False;
2:  GenerateRandom:["MyBooleanVar"|25];
```

### Remarks:
Depending on the variable type, `Number 1` and `Number 2` can have different meanings, as shown in this table:

|Type|Meaning|
|:---:|:---|
|String|`Number 2` is ignored. `Number 1` determines how many characters the random string should have.|
|Number|`Number 1` is the inclusive lower bound and `Number 2` is the inclusive upper bound of the range from which the random value is chosen. If `Number 1` is greater than `Number 2`, their position is switched automatically. Negative numbers are multiplied by -1.|
|Boolean|`Number 2` is ignored. `Number 1` determines the chance in percent (100 = 100%) that the result will be `true`.|
|Undefined|The Instruction is ignored.|

If a variable with the specified name doesn't already exist, this Instruction can automatically create that variable. If only `Number 1` is provided, the resulting variable will be of type String. If `Number 2` is provided as well, the resulting variable will be of type Number.

> It is important that you ONLY use the variable name for `Variable name` (i.e. not `#(VarName)`, only `VarName`).  
> Otherwise, you will pass the current value of the variable you want (or undefined if the variable doesn't exist) as the value for the parameter.

---
[Back to overview](index.md)
