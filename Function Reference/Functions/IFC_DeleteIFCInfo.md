# IFC_DeleteIFCInfo

## Description
Deletes all IFC data attached to the object.

```pascal
PROCEDURE IFC_DeleteIFCInfo(hObject : HANDLE, true);
```

```python
def vs.IFC_DeleteIFCInfo(hObject:HANDLE, true);
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to the object.|
|bDoUndo|BOOLEAN|Use undo or not.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE DeleteIFCInfo;
VAR
        bUndo          : BOOLEAN
        bOK            : BOOLEAN
        hObject        : HANDLE
BEGIN
        {We suggest that we have a handle to an object that has IFC data attached and we want to remove it and have the option to UNDO the change}
        bUndo          := TRUE;
	bOK            := IFC_DeleteIFCInfo( hObject, bUndo );
END;

RUN(DeleteIFCInfo);
```
==== Python ====
```python
# We suggest that we have a handle to an object that has IFC data attached and we want to remove it and have the option to UNDO the change
ok = vs.IFC_DeleteIFCInfo( hObject, True );
```

## Version
Availability: from Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
