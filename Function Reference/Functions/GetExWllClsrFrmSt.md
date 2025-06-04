# GetExWllClsrFrmSt

## Description
Gets the exclude wall closure from settings of a symbol definition, plug-in object style, or plug-in object.

```pascal
PROCEDURE GetExWllClsrFrmSt(
				hObject    : HANDLE;
				VAR left   : BOOLEAN;
				VAR right  : BOOLEAN;
				VAR top    : BOOLEAN;
				VAR bottom : BOOLEAN);
```

```python
def vs.GetExWllClsrFrmSt(hObject):
    return (left, right, top, bottom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|left|BOOLEAN|Returns the exclude wall closure from left setting.|
|right|BOOLEAN|Returns the exclude wall closure from right setting.|
|top|BOOLEAN|Returns the exclude wall closure from top setting.|
|bottom|BOOLEAN|Returns the exclude wall closure from bottom setting.|

## See Also
VS Functions:
[SetExWllClsrFrmSt](SetExWllClsrFrmSt.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
