# GetObjTypeProperties

## Description
Receives an object type and returns the properties of that object type

```pascal
FUNCTION GetObjTypeProperties(ObjectType : INTEGER): INTEGER;
```

```python
def vs.GetObjTypeProperties(ObjectType):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ObjectType|INTEGER|Object type whose properties are desired|

## Examples
```python
This function should return kTermProp for type kTermNode, kLineProp for kLineNode and so on for all existing object types that are defined in Objs.TDType.h.
```

```pascal
resultN := GetObjTypeProperties(1);
```
```python
import vs

# Receives an object type and returns the properties of that object type.
ObjectType = 0

resultN = vs.GetObjTypeProperties(ObjectType)
vs.Message('GetObjTypeProperties returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
