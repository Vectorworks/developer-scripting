# CC_AddSocket

## Description
Adds a socket to the given device. Orientation must be 'L' or 'R'. Returns the handle of the socket.

```pascal
FUNCTION CC_AddSocket(
				hDevice     : HANDLE;
				name        : STRING;
				type        : STRING;
				signal      : STRING;
				connector   : STRING;
				orientation : STRING) : HANDLE;
```

```python
def vs.CC_AddSocket(hDevice, name, type, signal, connector, orientation):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDevice|HANDLE||
|name|STRING||
|type|STRING||
|signal|STRING||
|connector|STRING||
|orientation|STRING||

## Version
Availability: from Vectorworks 2027

## Category
* [ConnectCAD](Categories/ConnectCAD.md)

