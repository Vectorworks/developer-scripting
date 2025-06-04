# GetVPClOvrdPenOpty

## Description
Retrieves the pen opacity for a class override. Opacity is in the range 0-100.

```pascal
FUNCTION GetVPClOvrdPenOpty(
				viewportHandle : HANDLE;
				className      : STRING): INTEGER;
```

```python
def vs.GetVPClOvrdPenOpty(viewportHandle, className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|Name of the class.|

## See Also
VS Functions:
[SetVPClOvrdPenOpty](SetVPClOvrdPenOpty.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
