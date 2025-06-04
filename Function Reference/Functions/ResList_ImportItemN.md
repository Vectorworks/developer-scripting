# ResList_ImportItemN

## Description
Import the currently selected item. doConflict: 0 - dont import; 1 - replace; 2 - rename; 3 - ask with UI. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
FUNCTION ResList_ImportItemN(
				uniqueID   : STRING;
				doConflict : LONGINT): HANDLE;
```

```python
def vs.ResList_ImportItemN(uniqueID, doConflict):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|doConflict|LONGINT|   |

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
