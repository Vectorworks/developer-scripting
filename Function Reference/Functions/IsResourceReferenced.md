# IsResourceReferenced

## Description
Returns whether a resource is workgroup referenced, and if so, the path to the source document is returned.

```pascal
FUNCTION IsResourceReferenced(
				resource     : HANDLE;
				VAR pathname : STRING) : BOOLEAN;
```

```python

def vs.IsResourceReferenced(resource):
    return (BOOLEAN, pathname)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|resource|HANDLE|Handle to the resource|
|pathname|STRING|On return, a string containing the path to the source document|

## Returns
Returns true if the resource is referenced, false otherwise.

## Examples
```pascal
PROCEDURE DoIt(h :HANDLE);

VAR

    pathname: STRING;

    isref: BOOLEAN;

BEGIN

    isref := IsResourceReferenced(h, pathname);

    IF (isref) THEN Message(pathname);

END;
```

## See Also
VS Functions:
[IsLayerReferenced](IsLayerReferenced.md)

## Version
Availability: from Vectorworks 2024

## Category
* [Object Info](../Categories/Object Info.md)

