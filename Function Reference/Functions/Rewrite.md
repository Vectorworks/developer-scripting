# Rewrite

## Description
Procedure Rewrite creates a new ASCII text file or opens an existing one prior to writing data to the file.  If the file exists, new data written to the file will overwrite any data currently within the file.

If the filename includes a fully qualified path, the path has to use the appropriate notation for the local operating system:
: <code>Macintosh HD:Applications:VectorWorks:Plug-Ins:Data:Notes.txt</code>
: <code>C:\Program Files\VectorWorks\Plug-Ins\Data\Notes.txt</code>

If the filename includes a path relative to the location of the VectorWorks executable, the subfolder delimiters have to be backslashes:
: <code>Plug-Ins\Data\Notes.txt</code>

If the filename does not include a path, the file is assumed to exist in the same folder as the VectorWorks executable.

```pascal
PROCEDURE Rewrite(fileName : STRING);
```

```python
def vs.Rewrite(fileName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of file.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    fileName :STRING; 
    major, minor, maintenance, platform :INTEGER;
BEGIN
    GetVersion(major, minor, maintenance, platform);
    IF platform = 1 THEN BEGIN
        fileName := '/Example.txt';
    END ELSE BEGIN
        fileName := 'C:Example.txt';
    END;
    ReWrite(fileName);
    WriteLn('example text');
    Close(fileName);
END;
RUN(Example);
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
#### Python ####
```python

```

```pascal
BEGIN
	Rewrite('Property Line Test.txt');
	WriteLn('Bearing Format      CAD');
	WriteLn('-----------------------');
	ValidBearingStrTest('N 10 E');
	ValidBearingStrTest('N 10.5 E');

BEGIN
	Rewrite (fileName);
	WriteLn (Concat (GetPlugInString (3018)), ':');
	WriteLn (Concat (GetPlugInString (3019), ' ', sDigits2 (area2,  kMinDisplayValue, kDisplayDigits), ' ', um2));
	WriteLn (Concat (GetPlugInString (3020), ' ', sDigits2 (perim2, kMinDisplayValue, kDisplayDigits), ' ', umD));
	Writeln ('');

BEGIN
	Rewrite (fileName);
	IF listAll THEN
		WriteLn (GetPlugInString (3014), GetFName)
	ELSE
		WriteLn (GetPlugInString (3015), GetFName);
```
```python
vs.Rewrite('file.txt')
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
