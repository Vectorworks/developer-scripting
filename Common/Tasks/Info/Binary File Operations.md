By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## Intro

The existing file functions prior to Vectorworks 2018 are now converted to support UTF-8. This means that they will output encoded characters, so working with CHAR becomes harder as CHAR is a single byte interpreted as text, so writing CHAR >= 127 is not possible.

This led to the addition of the following Vectorworks 2018 functions:
* [ReadBin](../../../Function%20Reference/Functions/ReadBin.md) – read the value as binary representation. The string version will ask for encoding and byte count
* [WriteBin](../../../Function%20Reference/Functions/WriteBin.md) – write the value as binary representation. The string version will ask for encoding
* [LenEncoding](../../../Function%20Reference/Functions/LenEncoding.md) – return byte count of a string in the specified encoding

```vs
PROCEDURE WriteBin( value : CHAR );      { write 1 byte }
PROCEDURE WriteBin( value : BOOLEAN );   { write 1 byte }
PROCEDURE WriteBin( value : REAL );      { write 8 bytes }
PROCEDURE WriteBin( value : INTEGER );   { write 2 bytes }
PROCEDURE WriteBin( value : LONGINT );   { write 4 bytes }

PROCEDURE WriteBin( value : STRING; encoding : INTEGER );
                { write sequence of bytes 
                  representing the string in the specified encoding.
                  No terminating 0 is written. }
                { Encoding: 0 – mac; 1 – win; 2 – system; 3 – UTF8; 4 – UTF16}

PROCEDURE WriteBin( value : DYNARRAY OF CHAR; encoding : INTEGER  ); {same as STRING}
```

```vs
PROCEDURE ReadBin( VAR value : CHAR );       { read 1 byte }
PROCEDURE ReadBin( VAR value : BOOLEAN );    { read 1 byte }
PROCEDURE ReadBin( VAR value : REAL );       { read 8 bytes }
PROCEDURE ReadBin( VAR value : INTEGER );    { read 2 bytes }
PROCEDURE ReadBin( VAR value : LONGINT );    { read 4 bytes }

PROCEDURE ReadBin (VAR  value : STRING; readBytes, encoding : INTEGER );
                { read sequence of bytes requested and return them as a string in the specified encoding. }
                { readBytes can be 0, then the first found zero byte (or bytes in UTF16 encoding) will terminate the string }
{  Encoding: 0 – mac; 1 – win; 2 – system; 3 – UTF8; 4 – UTF16}

PROCEDURE ReadBin ( VAR value : DYNARRAY OF CHAR; readBytes, encoding : INTEGER  ); {same as STRING}
```

These support the ‘:` formatting similar to the other filing functions. Described in “Data Formatting with Write and WriteLn” in
![VectorScriptGuide.pdf](../../../VectorScript/VectorScript%20Language%20Guide.pdf)

For example:
```vs
Write( 4 : 1 );
```

Will write 0x04 as a single byte.
