# GetTextStyleRef

## Description
Function GetTextStyleRef returns the text style for the referenced object. The integer returned is the internal index of the text style used by this object. <BR>
<BR>
If the text object is using class text style, this returns the effective style.  You should use the *TextStyleByClass* functions to check and preserve by-class behavior.

```pascal
FUNCTION GetTextStyleRef(objectId : HANDLE): LONGINT;
```

```python
def vs.GetTextStyleRef(objectId):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to object|

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
