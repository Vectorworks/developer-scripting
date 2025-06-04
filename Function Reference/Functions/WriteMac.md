# WriteMac

## Description
Outputs the specified data to an ASCII text file. The variable length parameter list specifies the data to be written to the file. 

Parameters may be any valid data type, and data types may be mixed in a single call to the procedure. WriteMac leaves the file pointer positioned at the end of the last data value written to the file; any data subsequently written to the file will be appended to the end of this value.

See the VectorScript Language Guide for details on formatting values using WriteLn.

```pascal
PROCEDURE WriteMac(z : ANY);
```

```python
def vs.WriteMac(z):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
==== VectorScript ====
```pascal
WriteMac(Value1);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [File I@O](../Categories/File%20IO.md)
