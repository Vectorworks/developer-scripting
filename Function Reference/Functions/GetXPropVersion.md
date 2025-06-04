# GetXPropVersion

## Description
Returns the version of the Extended Properties support currently running. To be used in case the way the calls work changes, and programmers have to account for the differences. 

See the <a href=http://www.vectorlab.info/index.php?title=Events>VectorLab article</a> on object events.

```pascal
PROCEDURE GetXPropVersion(VAR outVersion : LONGINT);
```

```python
def vs.GetXPropVersion():
    return outVersion
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outVersion|LONGINT|Output parameter.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
