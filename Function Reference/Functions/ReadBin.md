# ReadBin

## Description
Procedure ReadBin will read binary data from a currently open file. The variable length parameter list returns the read data in the specified parameters.

Supported data types include INTEGER (2-bytes), REAL (8-bytes), LONGINT (4-bytes), CHAR (1-byte) or STRING/DYNARRAY OF CHAR (see remarks).

The bytes will be written as little-endian.

Strings will require additional INTEGER parameter to specify encoding:
: 0 – mac
: 1 – win
: 2 – system
: 3 – UTF8
: 4 – UTF16

```pascal
PROCEDURE ReadBin(VAR z : ANY);
```

```python
def vs.ReadBin():
    return z
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## See Also
[WriteBin](WriteBin.md) | [Open](Open.md)

## Version
Availability: from VW 2018

## Category
* [File I@O](../Categories/File%20IO.md)
