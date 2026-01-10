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
|PropertyID|LONGINT| Property number. See [[VS:Object Events]]  |
|PropertyVal|CHAR| This is a number represented as character. Use Chr() - pascal or chr() - python functions |

## Remarks
[ptr 09/24/2019]
```pascal
CONST
  {ObjPropCharVS}
  kObjProp_SpecialEdit = 3; {PropertyID}
  kObjProp_SpecialEdit_Custom = 1; {PropertyVal}

  kObjProp_WidgetGroupMode = 81; {PropertyID}
  kPbjProp_WidgetGroupMode_Automatic = 2; {PropertyVal}

{ code }

res := SetObjPropCharVS( kObjProp_SpecialEdit, Chr(kObjProp_SpecialEdit_Custom) );
res := SetObjPropCharVS( kObjProp_WidgetGroupMode, Chr(kPbjProp_WidgetGroupMode_Automatic) );
```

```python
# ObjPropCharVS
kObjProp_SpecialEdit = 3  # PropertyID
kObjProp_SpecialEdit_Custom = 1  # PropertyVal

kObjProp_WidgetGroupMode = 81  # PropertyID
kPbjProp_WidgetGroupMode_Automatic = 2  # PropertyVal

# code

ok = vs.SetObjPropCharVS( kObjProp_SpecialEdit, chr(kObjProp_SpecialEdit_Custom) )
ok = vs.SetObjPropCharVS( kObjProp_WidgetGroupMode, chr(kPbjProp_WidgetGroupMode_Automatic) )
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
