# ActivateDV

## Description
Activates or deactivates the named Data Visualization for the object. The Data Visualization is appended to the end of the active list if it is not already there (activate), or removed (deactivate) from the list. If it is a Set, its elements are also activated/deactivated accordingly. Empty name means <None>: all Data Visualizations are deactivated for the object. Supported object types are:  nullptr or Design Layer (Data Visualization will be set for the Design environment); Viewport, Viewport Style, Saved View.

```pascal
FUNCTION ActivateDV(
				objHandle : HANDLE;
				dvName    : STRING;
				activate  : BOOLEAN) : BOOLEAN;
```

```python
def vs.ActivateDV(objHandle, dvName, activate):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objHandle|HANDLE|Data Visualization will be activated/deactivated for this object.|
|dvName|STRING|Name of the Data Visualization.|
|activate|BOOLEAN|Activate (true) or deactivate (false) the named Data Visualization for the object.|

## Returns
Returns true if the goal is achieved, false if an error happened (e.g. unknown name, unsupported object type). 

## See Also
VS Functions:
[GetActiveDVCount](GetActiveDVCount.md)| [GetActiveDVName](GetActiveDVName.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Data Visualizations](Categories/Data%20Visualizations.md)

