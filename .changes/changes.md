Updated 2022/09/18 WIP

---

**TO DO (3rd revision)**
- [ ] Check for termonology compliance.
- [ ] Add links and titles to Instruction names.
- [ ] Add "Instructions in this page" to footer.
- [ ] Change all example titles to 3rd person.
- [ ] Add psyche bar and health bar explaination to all relevant pages.

---

# Changelog

## In general
- Fixed various spelling and grammar mistakes.
- Rephrased unclear and oddly constructed sentences.
- Rearranged some text within the same section/subsection (when moving to other sections/subsections, it will be stated).
- Added more links to relevant pages.
- Changed some expressions to match the [Style Guide](https://github.com/WVam/toolscript-docs/blob/main/.changes/glossary.md).
  - By the way, I created a Style Guide to promote consistency.
- Corrected incorrect information.
- Improved offline compatibility.
  - Added a space before and after the second horizontal rule in each page.

When *Nothing significant* is written under a document changelog, it means that all changes fell under these categories.

## AACS-Code-Editor.md

- Rolled back to pre-placeholder version, with some adjustments:  
  - Changed formatting to match current formatting conventions.  
    - Added header and footer
  - Removed outdated information on linking and unlinking. 
  - Added a warning about possible outdated information.  
  - Added images back.
  - Updated some information to the current Code Editor version.
  - Changed some text to reflect the new example given for the `@Include` Instruction.

## Basics.md
- Formatted the technical information under 6. **Comment** as a note (block quote).
  - This information is now referred to in 1. **The semicolon**
    > If there is no semicolon at the end of an Instruction, the engine will skip the line and won't execute the Instruction (see 6. **Comments** for more info).

## Branch-Instructions.md
- Replaced `[AACS HERE]` with a `->Your AACS here<-`, as in Code Completion.
  - In the If section, it was replaced with a description of the conditions under which the script would be executed (e.g. `-> The Instructions contained here are executed if [Expression] returns True <-`.
- Specified that the `[VALUE]` in For should be positive (in case it wasn't obvious).

## Break.md
*Nothing significant*

## BreakLock.md
*Nothing significant*

## ChangeTextBox.md
- Default Value for the `Name` parameter was changed to:
    > See [Remarks](#changetextboxmd)

  The links is to the "Remarks" section in the actual page.
- Added an example regarding textboxes without a namebox.

## CrossExamC.md
- Commented out "INSTRUCTIONS" in the CrossExamination Instruction template.

## DecreaseHealth.md
*Nothing significant*

## DisplayEvidence.md
*Nothing significant*

## DisplayHealth.md
*Nothing significant*

## DiplayPopup.md
*Nothing significant*

## DisplayPopupWait.md
*Nothing significant*

## DisplayText.md
- Misspelled "Spelling".

## Examine.md
- Added Required and Default Value columns to Parameters table of Point (stated as ✓ and - respectively for all parameters) for clarity.
- Changed the description of the OFFSET parameter to make it clear that Spots are squares and not circles.
- Added links to Investigations page at the top and at the bottom next to the "Back to overview" link.

## FadeInBackground.md
*Nothing significant*

## FadeInCharacter.md
*Nothing significant*

## FadeInForeground.md
*Nothing significant*

## FadeInMusic.md
*Nothing significant*

## FadeInScene.md
*Nothing significant*

## FadeOutBackground.md
*Nothing significant*

## FadeOutCharacter.md
*Nothing significant*

## FadeOutForeground.md
*Nothing significant*

## FadeOutMusic.md
*Nothing significant*

## FadeOutScene.md
*Nothing significant*

## FinishAllInvestigation.md
*Nothing significant*

## FiniscCrossExam.md
*Nothing significant*

## FinishInvestigation.md
*Nothing significant*

## FinishMoodMatrix.md
*Nothing significant*

## FlashHealth.md
*Nothing significant*

## FlashScene.md
*Nothing significant*

## Frame.md
- Added explaination of syntax.

## GameOver.md
*Nothing significant*

## GenerateRandom.md
