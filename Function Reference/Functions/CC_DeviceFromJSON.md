# CC_DeviceFromJSON

## Description
Creates a device from a JSON string. The JSON may contain the fields: name, tag, make, model, category, description, labelSymbol, widthR, width, height, depth, power, weight, isModular, nSlots, and a socket group array. Returns the handle of the created device.

```pascal
FUNCTION CC_DeviceFromJSON(json : STRING) : HANDLE;
```

```python
def vs.CC_DeviceFromJSON(json):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|json|STRING||

## Version
Availability: from Vectorworks 2027

## Category
* [ConnectCAD](Categories/ConnectCAD.md)

