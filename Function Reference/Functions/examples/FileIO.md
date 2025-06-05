## VectorScript

```pascal
PROCEDURE Example;
VAR
  fileName :STRING; 
  major, minor, maintenance, platform :INTEGER;
BEGIN
  GetVersion(major, minor, maintenance, platform);
  IF platform = 1 THEN BEGIN
    fileName := 'Macintosh HD:Example.txt';
  END ELSE BEGIN
    fileName := 'C:\Example.txt';
  END;
  Append(fileName);
  WriteLn('example text');
  Close(fileName);
END;
RUN(Example);
```

### Writing binary data

Write of ARRAY OF INTEGER will write two bytes per INTEGER. So, 10 bytes will be written for 'arr'.  
This code will produce file with the following bytes (hex): `01 02 FF FE 00 00 00 00 00 00`

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

## Python

```python
def Example():
	major, minor, maintenance, platform = vs.GetVersion()
	if platform == 1:
		fileName = 'Macintosh HD:Example.txt'
	else:
		fileName = 'D:\\Example.txt'
	vs.Append(fileName)
	vs.WriteLn('example text')
	vs.Close(fileName)
Example()
```
