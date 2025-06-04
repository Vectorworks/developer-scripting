# GetTextStyleRefN

## Description
GetTextStyleRefN returns the text style reference at a specified position within the text object. Reference 0 means Un-Styled.<BR>
<BR>
If the text object is using class text style, this returns the effective style.  You should use the *TextStyleByClass* functions to check and preserve by-class behavior.

```pascal
FUNCTION GetTextStyleRefN(
				objectId : HANDLE;
				position : INTEGER): LONGINT;
```

```python
def vs.GetTextStyleRefN(objectId, position):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to text object|
|position|INTEGER|Position in text string, zero-based.|

## See Also
VS Functions:
[SetTextStyleRef](SetTextStyleRef.md) 
| [GetTextStyleRef](GetTextStyleRef.md) 
| [SetTextStyleRefN](SetTextStyleRefN.md) 
| [GetTextStyleRefN](GetTextStyleRefN.md) 
| [SetTextStyleByClass](SetTextStyleByClass.md) 
| [SetTextStyleByClassN](SetTextStyleByClassN.md) 
| [IsTextStyleByClass](IsTextStyleByClass.md) 
| [IsTextStyleByClassN](IsTextStyleByClassN.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
