# vstGetInitObject

## Description
Return HANDLE to the object that this tool should copy. Part of 'similar object createion'. Used inside kToolInitByObject event.

```pascal
FUNCTION vstGetInitObject(message1 : LONGINT): HANDLE;
```

```python
def vs.vstGetInitObject(message1):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message1|LONGINT|   |

## Examples
le can be found at [[VS:Similar_Objects_Creation#Tool_Part]]

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
