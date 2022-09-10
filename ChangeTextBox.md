[Back to overview](index.md)

---
# ChangeTextBox (CTB)

---

### Description
Changes the textbox to use custom images in the "UI" folder.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The file name without the file extension.|✓|See **Remarks**|

### Examples:
#### Example #1: Changing the custom textbox visuals to a custom file called "Dual Destinies.png" in the "UI" folder.
```
1:  ...
2:  ChangeTextBox:["Dual Destinies"];
3:  ...
```

#### Example #2: Resetting the textbox visuals to default.
```
1:  ...
2:  CTB:[-];
3:  ...
```

### Remarks:
This option changes the textbox visuals for all following [DisplayText](DisplayText.md) Instructions, so you only have to call it once, for example at the beginning of the script. If you pass the null character `-`, the textbox will be changed to the default style again. 

To use an image, you have to save it in the "UI" folder of the theme you wish to use.  
If your textbox also has a version without the namebox, add the image with the same name as the textbox with the namebox + "_NoName".
> For example, if the image your custom textbox **with** a namebox is named "Dual Destinies.png", add the image for your custom textbox **without** the namebox as "Dual Destinies_NoName.png". After that, if you run the following Instructions:
> ```
> 1:  ChangeTextBox:["Dual Destinies"];
> 2:  DisplayText:[-|"That attorney...#[200] He is so mean!"];
> ```
> the DisplayText Instruction at line 2 will use the "Dual Destinies_NoName.png".

You can specify a textbox directly in the Theme, as well.

---
[Back to overview](index.md)
