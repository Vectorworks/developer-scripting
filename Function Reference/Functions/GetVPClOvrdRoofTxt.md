# GetVPClOvrdRoofTxt

```pascal
PROCEDURE GetVPClOvrdRoofTxt(
				viewportHandle     : HANDLE;
				className          : STRING;
				VAR topMaterial    : LONGINT;
				VAR dormerMaterial : LONGINT);
```

```python
def vs.GetVPClOvrdRoofTxt(viewportHandle, className):
    return (topMaterial, dormerMaterial)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class override|
|topMaterial|LONGINT|The material of the top|
|dormerMaterial|LONGINT|The material of the dormer|

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
