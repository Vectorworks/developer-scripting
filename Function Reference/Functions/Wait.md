# Wait

## Description
Procedure Wait delays execution in VectorScript for a specified number of seconds.

When paused, a VectorScript routine stops at the point where Wait is encountered.

```pascal
PROCEDURE Wait(seconds : INTEGER);
```

```python
def vs.Wait(seconds):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|seconds|INTEGER|Number of seconds to pause script execution.|

## Examples
#### VectorScript ####
```pascal
Wait(3);
{pauses execution for 3 seconds}
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
