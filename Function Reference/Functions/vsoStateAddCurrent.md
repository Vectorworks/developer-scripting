# vsoStateAddCurrent

## Description
Allows to add the current state during event 44 (kObjOnAddState). 

See [[VS:Parametric_State_Notifications#Receiving_States:_kParametricAddState_(44)]]

```pascal
FUNCTION vsoStateAddCurrent(
				hObj    : HANDLE;
				message : LONGINT): LONGINT;
```

```python
def vs.vsoStateAddCurrent(hObj, message):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |
|message|LONGINT|   |

## Remarks
{ quoting Vlado: }  During event 44 the user MUST only call VS:vsoStateAddCurrent nothing else!

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
