# GetTextSize

## Description
Procedure GetTextSize returns the text point size at a specified position within the referenced text object. 1 point = 1/72&quot;. 

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

```pascal
FUNCTION GetTextSize(
				TextHd   : HANDLE;
				Position : INTEGER): REAL;
```

```python
def vs.GetTextSize(TextHd, Position):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|Position|INTEGER|Position in text string.|

## Remarks
The result was previously an integer, but is now a floating point value.

Here's a snippet that shows how to get the text size that has been assigned to a PIO from the text menu:
<code lang="pas">
pioTextSize := ((GetObjectVariableReal(pioHandle, 17) / GetLScale(GetLayer(pioHandle))) * 72) / 25.4;
</code>


Example:
<code lang="pas">
PROCEDURE Example;
CONST
theSizeToSelect = 10;
VAR
criteria :STRING;

PROCEDURE SelectBySize(h :HANDLE);
BEGIN
IF GetTextSize(h, 0) = theSizeToSelect THEN SetSelect(h);
END;

BEGIN
DSelectAll;
criteria := '(T=10)';
ForEachObject(SelectBySize, criteria);
END;
RUN(Example);
</code>

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
