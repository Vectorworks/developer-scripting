# GetVPClOvrdName

## Description
Gets the name for the override at a particular index in the override list.

```pascal
FUNCTION GetVPClOvrdName(
				viewportHandle : HANDLE;
				index          : INTEGER): STRING;
```

```python
def vs.GetVPClOvrdName(viewportHandle, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|index|INTEGER|The index into the class override list.|

## See Also
VS Functions:
[GetVPClOvrdCount](GetVPClOvrdCount.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
