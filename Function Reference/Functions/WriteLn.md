# WriteLn

## Description
Procedure WriteLn outputs the specified data to an ASCII text file. The variable length parameter list specifies the data to be written to the file. 

Parameters may be any valid data type, and data types may be mixed in a single call to the procedure. A carriage return is appended to the end of the line of data, so that the file pointer is at the beginning of a new line in the file, and any data written to the file after the procedure call will be on the new line.

See the VectorScript Language Guide for details on formatting values using WriteLn.

```pascal
PROCEDURE WriteLn(z : ANY);
```

```python
NOT AVAILABLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Remarks
From Raymond Mullin:

1 - Writing NUL (chr(0)) is impossible. Nothing happens.

2 - Writing LF changes the value to CR (LineFeed -&gt; CarriageReturn, or 0A -&gt; 0D hex). 

3 - Reading LF &amp; CR (0A &amp; 0D hex) returns the SPACE character (20 hex).

4 - String variables cannot contain NUL characters as the NUL is used to delimit the end of the string (thanks Pat).

5 - An array of characters can have NUL as one or more of its elements.

6 - Writing the array to a file will fail to export the NUL values. 

7 - If an array of characters is written to a file, the number of characters in the file will be less than the array length by the number of NULS in the array.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
CONST
Vendor = 'ACME';
Price = 123.45;
Tax = 1.07;
BEGIN
ReWrite('Output.txt');
WriteLn('Mfr/Cost: ', Vendor, '/', Price + Tax);
Close('Output.txt');
END;
RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[WriteLnMac](WriteLnMac.md)

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
