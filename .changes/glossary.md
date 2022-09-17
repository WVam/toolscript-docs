# Style guide 

The AACS Documentation was changed to follow this style guide. Most glossary-like parts were extrapolated from indications by the developer as well as use of words throughout the documentation.

# Formatting
- Bold is used for emphasis.
- Monospace is used for parameters and charactres/groups of character that are significant to the syntax (e.g.: `->`).
  - It's also used for Instructions written with their parameters and final semicolon.
- Code blocks are used for script.
- Block quotes are used for notes.
- Headers are used for headers.
- Instruction names always link to their respective page.

Higlight "not" or command words when particularly important by writing them in uppercase and bold (**NOT**). For "cannot", use "**CANNOT**".

## Structure-related terminology
Here, this documentation's established terminology has been changed to match more widespread terminology.
- What is contained in a single page is called a **page**.
- Everything under a h2 header up until the next h2 header is called a **section**.
- Everything under a header of level h3 or lower up until the next header of the same or higher level is called a **subsection**.

## Commands and instructions

### Consistency

To express certain concepts, only certain words will be used.

- **abbr.**: introduces an abbreviation.
- **e.g.**: introduces an example in brackets.
- **Example:** / **Examples:** : introduces an example in block quotes.
- **for example**/**for instance**: introduces an example outside of brackets.
- **i.e.**: introduces an explaination.

### "if" and "whether"
Use "if" to introduce a **condition**.

> Example:
> 
> "If you run the Break Instruction, the game will wait for player input in order to continue."

Use "whether... or..." and "whether or not..." to introduce an **indirect interrogative clause**.

 > Examples:
 > 
 > "**Whether or not** a string contains meaningful words is irrelevant"  
 > "**Whether** you set the parameter to a number **or** to a string is irrelevant"

Use "regardless of whether... or..." and "regardless of whether or not..." to introduce **concessive clauses**.

 > Examples:
 > 
 > Do **NOT** write this: "The script will run regardless of \**if* you passed the right parameter."  
 > Write **THIS**: "The script will run **regardless of whether or not** you passed the rigth parameter."

### "may"
Do **NOT** use the verb "may". It can be interpreted as meaning both ability and possibility. For ability, use "can". For possibility, use "might".

> Example:  
> 
> Do **NOT** write this: "This Instruction \**may* cause the game to crash".  
> Write **THIS**: "This Instruction **might** cause the game to crash".  
> 
> Do **NOT** write this: "You \**may* substitute a parameter with the character `-`."  
> Write **THIS**: "You **can** substitute a parameter with the character `-`."

### "to"

If the meaning of "to" used to express a purpose might be ambiguous to a hasty reader, replace it with "in order to".

## Cross Examinations

Use *Cross Examination* when:
- referring to the gameplay mechanic;
  > e.g. "Cross Examinations allow the player to find contradictions in a witness' testimony"
- referring to the gameplay sequence.
  > e.g. "During Cross Examinations, a player may present evidence"

Use *the CrossExamination Instruction/Container* when:
- referring to the specifics of the Instruction;
  > e.g. "The CrossExamination Instruction has two parameters"
- referring to the contents of the the CrossExamination Container.
  > e.g. "The Statements in the CrossExamination Container"

Use *cross-examination* when:
- referring to the act of cross-examining a witness;
  > e.g. "The Court Record is an essential tool for players during their cross-examination of a witness"

The verb *cross-examine* is used (not \**Cross Examine*).

## Investigations

Use *Investigation* when:
- referring to the gameplay mechanic;
  > e.g. "Investigations allow the player to find evidence at the crime scene"
- referring to the gameplay sequence.
  > e.g. "During Investigations, a player may present evidence"

Use *the Investigation Instruction/Container* when:
- referring to the specifics of the Instruction;
  > e.g. "The Investigation Instruction only has one parameter"
- referring to the contents of the the CrossExamination Container.
  > e.g. "Moving is used in the Investigation Container"

Use *investigation* when:
- referring to the act of a player investigating;
  > e.g. "Players might find evidence during their investigation of the crime scene"

The verb *investigate* is used (not \**Investigate*).

## Mood Matrix

*Mood Matrix* is singulare tantum. It should never be used as a plural or in contexts where it can be pluralized.

Use *the Mood Matrix* when
- referring to the gameplay mechanic;
  > e.g. "The Mood Matrix allows the player to visualize a person's true emotions"

Use *Mood Matrix sequence* when:
- referring to the gameplay sequence.
  > e.g. "During Cross Examinations, a player may present evidence"

Use *the MoodMatrix Instruction/Container* when:
- referring to the specifics of the Instruction;
  > e.g. "The MoodMatrix Instruction only has one parameters"
- referring to the contents of the the MoodMatrix Container.
  > e.g. "The Statements in the MoodMatrix Container"

There is no term for to the act of a player using the Mood Matrix on a witness. *(Suggestion: therapy session (n.), conduct a therapy session on (v.))*

## Oddly capitalized words

- Branch (Instruction)
- Code Completion
- Container (Instruction)
- Court Record
- Frame
- Hybrid Instruction
- Instruction
- Psyche Lock
- Regular Instruction
- Statement
- Template
- Theme

## Other stuff

- When the name of an Instruction can be confused with something else that is not an Instruction, use "the INSTRUCTION Instruction"
  - If INSTRUCTION is a Container/Branch, you can use "the INSTRUCTION Container"/"the INSTRUCTION Branch" 
  - 
