# ActivateDVSetElem

## Description
Activates or deactivates the named element for the named Data Visualizations set for the object, provided the set is currently active for the object. Empty set or element name is an error. Supported object types are:  nullptr or Design Layer (Data Visualizations set element will be activated/deactivated for the Design environment); Viewport, Viewport Style, Saved View.<BR>


```pascal
FUNCTION ActivateDVSetElem(
				objHandle : HANDLE;
				setName   : STRING;
				elName    : STRING;
				activate  : BOOLEAN) : BOOLEAN;
```

```python
def vs.ActivateDVSetElem(objHandle, setName, elName, activate):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objHandle|HANDLE|Data Visualizations set element will be activated/deactivated for this object.|
|setName|STRING|Name of the Data Visualizations set.|
|elName|STRING|Name of the element.|
|activate|BOOLEAN|activate Activate (true) or deactivate (false) the named Data Visualization for the object.|

## Returns
Returns true if the goal is achieved, false if an error happened (e.g. unknown name, element does not belong to the set, set is not active for  the object, unsupported object type). <BR>


## See Also
VS Functions:
[GetActDVSetElemCount](GetActDVSetElemCount.md)| [GetActDVSetElemName](GetActDVSetElemName.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Data Visualizations](Categories/Data%20Visualizations.md)

