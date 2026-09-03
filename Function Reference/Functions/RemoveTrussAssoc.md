# RemoveTrussAssoc

## Description
Removes the association between the side arm and it's rigging.

```pascal
PROCEDURE RemoveTrussAssoc(handle : HANDLE);
```

```python
def vs.RemoveTrussAssoc(handle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE||

## Examples
```pascal
BEGIN
	RemoveTrussAssoc( SelObjHandles[gNumConverted] );
END
```
```python
import vs

# Removes the association between the side arm and it's rigging.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.RemoveTrussAssoc(handle)
```

## Version
Availability: from Vectorworks 2026

## Category
* [Spotlight](../Categories/Spotlight.md)
