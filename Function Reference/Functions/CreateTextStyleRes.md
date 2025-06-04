# CreateTextStyleRes

## Description
Creates a new text style resource with the specified name.  A handle to the new resource is returned.  Once the resource is created the attributes of the text style resource should be set appropriately.

```pascal
FUNCTION CreateTextStyleRes(name : STRING): HANDLE;
```

```python
def vs.CreateTextStyleRes(name):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name for the new text style.|

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
