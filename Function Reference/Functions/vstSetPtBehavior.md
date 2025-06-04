# vstSetPtBehavior

```pascal
PROCEDURE vstSetPtBehavior(inStatusType : LONGINT);
```

```python
def vs.vstSetPtBehavior(inStatusType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStatusType|LONGINT|   |

## Remarks
0 -  the tool will collect two points using click drag gesture

1 - the tool will collect one point

2 -  the tool will collect two points using user click-click/drag pref setting

3 -  the tool will collect three points

4 -  the tool will collect multiple points - double-click completes

101 - the tool will draw a box

102 - the tool will draw an Ellipse

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
