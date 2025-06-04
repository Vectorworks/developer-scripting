# GetKeyDown

## Description
Procedure GetKeyDown pauses execution of a VectorScript routine until a key is pressed by the user. When the key is pressed, the ASCII code of the key is returned.

```pascal
PROCEDURE GetKeyDown(VAR asciiCode : LONGINT);
```

```python
def vs.GetKeyDown():
    return asciiCode
```

## Parameters
|Name|Type|Description|
|---|---|---|
|asciiCode|LONGINT|ASCII code of key pressed.|

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
