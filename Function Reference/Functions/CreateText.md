# CreateText

## Description
Procedure CreateText creates a new text object in a VectorWorks document. The text object is created using the current pen position and default attributes.

```pascal
PROCEDURE CreateText(theText : DYNARRAY[] of CHAR);
```

```python
def vs.CreateText(theText):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|DYNARRAY[] of CHAR|Text string.|

## Remarks
*\_c\_*, 2015.12.19: If you draw text, it is important to have a proper text size on the document or you'll see the error "An incorrect object is described".
```pascal
PushAttrs;
	NameClass(ClassList(1));
	PenPat(1);
	FillPat(0);
	PenFore(0, 0, 0);
	TextSize(9); { avoid accidental small text size rising the error "An incorrect object is described" }
	CreateText('Text');
PopAttrs;
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    Txt   :ARRAY [1..100] of STRING;
    Outpt :DYNARRAY[] of CHAR;
    i     :INTEGER;
BEGIN
    FOR i := 1 TO 5 DO txt[i] := 'asdf';
    i := 2;
    Outpt := Txt[1];
    WHILE Txt[i] &lt;&gt; '' DO BEGIN
        OutPt := Concat(Outpt, Chr(13), Txt[i]);
        i := i + 1;
    END;
    Layer('Text');
    CreateText(Outpt);
    Layer('Layer-1');
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	txt = []
	for i in range(0,4):
		txt.append('asdf')
	txt.append("")
	i = 1
	Outpt = txt[0]
	while txt[i] != "":
		OutPt = vs.Concat(Outpt, vs.Chr(13), txt[i])
		i = i + 1
		
	vs.Layer('Text')
	vs.CreateText(Outpt)
	vs.Layer('Layer-1')

Example()
```

## See Also
VS Functions:
[BeginText](BeginText.md) 
| [EndText](EndText.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
