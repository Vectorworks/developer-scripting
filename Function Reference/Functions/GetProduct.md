# GetProduct

## Description
Identifies what NNA products and product packages are available in the current product installation.

Obsolete as of 10. Use GetEnabledModules instead.

```pascal
PROCEDURE GetProduct(
				VAR product : INTEGER;
				VAR modules : LONGINT);
```

```python
def vs.GetProduct():
    return (product, modules)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|product|INTEGER|Product index.|
|modules|LONGINT|Package index.|

## Remarks
Retrieves information that identifies what vertical market product (if any) is currently running, and which add-ons (modules) are currently available (if any).


Should mark this as obsolete.

## See Also
VS Functions:
[GetEnabledModules](GetEnabledModules.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Utility](../Categories/Utility.md)
