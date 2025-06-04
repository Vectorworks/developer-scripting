# GetCompManualBound

## Description
Gets the manual bound of a component in an object.

```pascal
FUNCTION GetCompManualBound(
				object          : HANDLE;
				componentIndex  : INTEGER;
				VAR manualBound : INTEGER): BOOLEAN;
```

```python
def vs.GetCompManualBound(object, componentIndex):
    return (BOOLEAN, manualBound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|manualBound|INTEGER|Returns the manual bound of the component.  0 - Roof edge 1 - Roof axis line|

## See Also
VS Functions:
[SetCompManualBound](SetCompManualBound.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
