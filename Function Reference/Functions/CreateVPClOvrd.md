# CreateVPClOvrd

## Description
Creates a new override for the specified class in the specified viewport. The override is initially populated with the class's current properties.

```pascal
PROCEDURE CreateVPClOvrd(
				viewportHandle : HANDLE;
				className      : STRING);
```

```python
def vs.CreateVPClOvrd(viewportHandle, className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|The name of the class.|

## See Also
VS Functions:
[RemoveVPClOvrd](RemoveVPClOvrd.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
