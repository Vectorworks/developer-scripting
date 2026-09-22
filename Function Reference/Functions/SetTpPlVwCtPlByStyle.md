# SetTpPlVwCtPlByStyle

## Description
Sets whether the Top/Plan view cut plane of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION SetTpPlVwCtPlByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN) : BOOLEAN;
```

```python
def vs.SetTpPlVwCtPlByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the Top/Plan view cut plane is by style.|

## Returns
Whether the call succeeded.

## See Also
VS Functions:
[GetTpPlVwCtPlByStyle](GetTpPlVwCtPlByStyle.md)

## Version
Availability: from Vectorworks 2026.2

## Category
* [Objects - Custom](Categories/Objects%20-%20Custom.md)

