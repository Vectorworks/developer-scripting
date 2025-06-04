# Name2Index

## Description
Function Name2Index returns the internal index number for the specified object.

```pascal
FUNCTION Name2Index(name : STRING): LONGINT;
```

```python
def vs.Name2Index(name):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of object.|

## Remarks
Returns the internal index for the object associated with the specified name.

(Joel Sciamma 2006.08.11): If the name does not exist, Name2Index returns zero.

## Examples
#### VectorScript ####
```pascal
NameIndex := Name2Index('objectName');
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetSkylight](SetSkylight.md) 
| [CreateSkylight](CreateSkylight.md) 
| [AddCavity](AddCavity.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Object Names](../Categories/Object%20Names.md)
