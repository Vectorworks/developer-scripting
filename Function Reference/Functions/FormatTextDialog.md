# FormatTextDialog

## Description
Displays the text formatting dialog and returns the selected text formatting options.


{| class="wikitable_c"
|+ Table - Text Style
! Style !! Constant
|-
| Plain
| 0
|-
| Bold
| 1
|-
| Italic
| 2
|-
| Underline
| 4
|-
| Outline
| 8
|-
| Shadowed
| 16
|}

{| class="wikitable_c"
|+ Table - disableMask Values
! Description !! Constant
|-
| Font
| 1
|-
| Size
| 2
|-
| Spacing
| 4
|-
| Style
| 8
|-
| hAlign
| 16
|-
| vAlign
| 32
|}

```pascal
PROCEDURE FormatTextDialog(
				VAR fontName   : STRING;
				VAR style      : INTEGER;
				VAR size       : REAL;
				VAR spacing    : INTEGER;
				VAR leading    : REAL;
				VAR hAlignment : INTEGER;
				VAR vAlignment : INTEGER;
				disableMask    : INTEGER);
```

```python
def vs.FormatTextDialog(fontName, style, size, spacing, leading, hAlignment, vAlignment, disableMask):
    return (fontName, style, size, spacing, leading, hAlignment, vAlignment)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fontName|STRING|The name of the selected font.|
|style|INTEGER|The selected style options.  0 for plain text.  Bit 1 is on for bold, bit 2 for italic, bit 3 for underline, bit 4 for outline and bit 5 for shadow.|
|size|REAL|The selected size (in points).|
|spacing|INTEGER|The selected spacing option.  0 for custom leading, 2 for single spacing, 3 for 1 1/2 spacing and 4 for double spacing.|
|leading|REAL|The selected leading value (in points) for custom spacing or -1 for a standard spacing.|
|hAlignment|INTEGER|The selected horizontal alignment options.  0 for general justify (used only on worksheets), 1 for left, 2 for center and 3 for right.|
|vAlignment|INTEGER|The selected vertical alignment options.  1 for top, 2 for top baseline, 3 for center, 4 for bottom baseline and 5 for bottom.|
|disableMask|INTEGER|Disables controls on the dialog.  Bit 1 disables font name, bit 2 size, bit 3 spacing, bit 4 style, bit 5 h align, bit 6 v align.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR 
font    :STRING; 
style   :INTEGER;
size    :REAL;
spacing :INTEGER; 
leading :REAL;
hAlign  :INTEGER;
vAlign  :INTEGER;
disable :INTEGER;
BEGIN
{Set some dialog defaults.}
font := 'Arial';
style := 1;
size := 12;
spacing := 2;

{Bit values for disableMask: 
1: font
2: size
4: spacing
8: style
16: hAlign
32: vAlign}
disable := 32;

{Now get the user's selections.}
FormatTextDialog(font, style, size, spacing, leading, hAlign, vAlign, disable);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
    #{Set some dialog defaults.}
    font = 'Arial'
    style = 1
    size = 12
    spacing = 2
    leading = -1
    hAlign = 1
    vAlign = 1
    #{Bit values for disableMask: 
    #1: font
    #2: size
    #4: spacing
    #8: style
    #16: hAlign
    #32: vAlign}
    disable = 32

    #{Now get the user's selections.}
    font, style, size, spacing, leading, hAlign, vAlign = vs.FormatTextDialog(font, style, size, spacing, leading, hAlign, vAlign, disable)

Example()
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
