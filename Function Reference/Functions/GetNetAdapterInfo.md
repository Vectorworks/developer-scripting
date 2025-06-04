# GetNetAdapterInfo

## Description
Return information about the network adapter

```pascal
FUNCTION GetNetAdapterInfo(
				adapterIndex   : INTEGER;
				VAR outMacAddr : STRING): BOOLEAN;
```

```python
def vs.GetNetAdapterInfo(adapterIndex):
    return (BOOLEAN, outMacAddr)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|adapterIndex|INTEGER|   |
|outMacAddr|STRING|   |

## Remarks
from Vlado originally: index '1' is for your first network card. '2' would be your next
one, if you have more than one. The function should return FALSE when
the card with this index doesn't exist, so you can handle cases with
many cards."

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
