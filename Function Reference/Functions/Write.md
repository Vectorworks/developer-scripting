# Write

## Description
Procedure Write outputs the specified data to an ASCII text file. The variable length parameter list specifies the data to be written to the file. 

Parameters may be any valid data type, and data types may be mixed in a single call to the procedure. Write leaves the file pointer positioned at the end of the last data value written to the file; any data subsequently written to the file will be appended to the end of this value.

See the VectorScript Language Guide for details on formatting values using WriteLn.

```pascal
PROCEDURE Write(z : ANY);
```

```python
def vs.Write(z):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
==== VectorScript ====
```pascal
Write(Value1);
```
Writing binary data:
:Write of ARRAY OF INTEGER with write two bytes per INTEGER. So, 10 bytes will be written for 'arr'.
:This code will produce file with the following bytes(hex): 01 02 FF FE 00 00 00 00 00 00
```pascal
arr : ARRAY [1..5] OF INTEGER;
	
  FUNCTION MixBytes(b1, b2: INTEGER) : INTEGER;
  BEGIN
    MixBytes := b1 + b2 * 256;
  END;
BEGIN
  arr[1] := MixBytes( 1, 2 );
  arr[2] := MixBytes( 255, 254 );
  Write(arr);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
