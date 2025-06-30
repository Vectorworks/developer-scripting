# CreateWS

## Description
Creates a new worksheet in a VectorWorks document.

```pascal
FUNCTION CreateWS(
				name    : STRING;
				rows    : INTEGER;
				columns : INTEGER): HANDLE;
```

```python
def vs.CreateWS(name, rows, columns):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the worksheet.|
|rows|INTEGER|The number of rows in the worksheet.|
|columns|INTEGER|The number of columns in the worksheet.|

## Remarks
Creates a new worksheet object with the specified name and number of rows and columns.
If the name is in use, a legal available name based on the specified name will be used instead.
The number of rows must be >= 1 and <= 4094.
The number of columns must be >= 1 and <= 256.
NOTE: To create an on-drawing worksheet object, pass a worksheet handle to [CreateWSImage ](CreateWSImage .md).

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
