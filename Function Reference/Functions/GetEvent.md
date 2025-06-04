# GetEvent

## Description
See [[VS:Object Events]].

```pascal
FUNCTION GetEvent() :LONGINT;
```

```python
def vs.GetEvent():
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
||   |   |

## Remarks
[Ptr 09/23/2019]
<code lang = "pas">
CONST
  {Event ID's}
  kEventID_Reset = 3;
  kEventID_OnObjPref = 4;
  kEventID_OnInitProperties = 5;
  kEventID_OnDoubleClick = 7;
  kEventID_OnUIButtonHit = 35;
  kEventID_OnAddState = 44;
</code>
<code lang = "py">
# Event ID's
kEventID_Reset = 3
kEventID_OnObjPref = 4
kEventID_OnInitProperties = 5
kEventID_OnDoubleClick = 7
kEventID_OnUIButtonHit = 35
kEventID_OnAddState = 44
</code>

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
