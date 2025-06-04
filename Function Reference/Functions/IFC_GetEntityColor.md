# IFC_GetEntityColor

## Description
Gets the default color for an IFC entity type

```pascal
FUNCTION IFC_GetEntityColor(
				inStrIfcType  : STRING;
				VAR outRed    : INTEGER;
				VAR outGreen  : INTEGER;
				VAR outBlue   : INTEGER;
				VAR outTransp : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetEntityColor(inStrIfcType):
    return (BOOLEAN, outRed, outGreen, outBlue, outTransp)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrIfcType|STRING|IFC Entity type.|
|outRed|INTEGER|Out parameter. Red Value of RGB color model.|
|outGreen|INTEGER|Out parameter. Green Value of RGB color model.|
|outBlue|INTEGER|Out parameter. Blue Value of RGB color model.|
|outTransp|INTEGER|Out parameter. Transepransy value.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	red   : INTEGER;
        green : INTEGER;
        blue  : INTEGER;
        transp: INTEGER;
	ok    : BOOLEAN;
begin
	ok := IFC_GetEntityColor('IfcWall', red, green, blue, transp);
end;

Run(Test);
```
#### Python ####
```python
ok = vs.IFC_GetEntityColor('IfcWall', red, green, blue, transp)
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
