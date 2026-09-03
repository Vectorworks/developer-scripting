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

## Examples
```pascal
GetKeyDown(1);
```
```python
import vs

# Procedure GetKeyDown pauses execution of a VectorScript routine until a key
# is pressed by the user.
result = vs.GetKeyDown()
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
