# GetCustomObjectSelectionGroup

## Description
Access the handle to selection group. This group contains geometry that defines the selection and pre-selection indication of this object.

See [[VS:Parametric Custom Selection Indication]] for more info.

```pascal
FUNCTION GetCustomObjectSelectionGroup(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetCustomObjectSelectionGroup(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to custom object.|

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
