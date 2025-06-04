# SetObjPropCharVS

## Description
See [[VS:Object Events]].

```pascal
FUNCTION SetObjPropCharVS(
				PropertyID  : LONGINT;
				PropertyVal : CHAR):BOOLEAN;
```

```python
def vs.SetObjPropCharVS(PropertyID, PropertyVal):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|PropertyID|LONGINT|   |
|PropertyVal|CHAR|   |

## Remarks
[ptr 09/24/2019]
<code lang="pas">
CONST
  {ObjPropCharVS}
  kObjProp_SpecialEdit = 3; {PropertyID}
  kObjProp_SpecialEdit_Custom = '1'; {PropertyVal}

  kObjProp_WidgetGroupMode = 81; {PropertyID}
  kPbjProp_WidgetGroupMode_Automatic = '2'; {PropertyVal}
</code>
<code lang="py">
# ObjPropCharVS
kObjProp_SpecialEdit = 3  # PropertyID
kObjProp_SpecialEdit_Custom = "1"  # PropertyVal

kObjProp_WidgetGroupMode = 81  # PropertyID
kPbjProp_WidgetGroupMode_Automatic = "2"  # PropertyVal
</code>

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
