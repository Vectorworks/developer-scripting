# SetCntrlPtVis

## Description
Sets the visibility of the specified control point.

```pascal
PROCEDURE SetCntrlPtVis(
				inCustomObj     : HANDLE;
				inContrlPtIndex : INTEGER;
				inIsVisible     : BOOLEAN);
```

```python
def vs.SetCntrlPtVis(inCustomObj, inContrlPtIndex, inIsVisible):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inCustomObj|HANDLE|   |
|inContrlPtIndex|INTEGER|   |
|inIsVisible|BOOLEAN|   |

## Remarks
[Joshua Benghiat 2006/12/14]: 

inContrlPtIndex is 1 based and matches the index in the name of the control point (i.e. CONTROLPOINT01X).

The procedure works both inside the PIO definition and from an external command.

The visibility status does not reset itself.  That is, if you want to toggle visibility on and off, you need something like: IF boo THEN SetCntrlPtVis(obHan, 1, TRUE) ELSE SetCntrlPtVis(obHan, 1, FALSE); 

[Julian Carr, 2007/3/23]: ...or more succinctly  SetCntrlPtVis(ParmHan, 1, boo);

[David Bengali, 2020/06/26]: index seems to match not the name of the control point parameter, but its ordinal position in the PIO definition. e.g., if CONTROLPOINT03X, CONTROLPOINT03Y are listed first and CONTROLPOINT01X, CONTROLPOINT02X are listed next, possibly with some non control-point params in between, controlpoint03 will respond to index 1 and controlpoint01 will respond to index 2. (Observed with python, not tested with VS)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
