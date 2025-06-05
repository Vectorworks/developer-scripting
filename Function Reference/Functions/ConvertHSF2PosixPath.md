# ConvertHSF2PosixPath

## Description
MacIntosh only!

Converts HSF (using ':' as delimiter) file path to Posix (using '/' as delimiter) file path.

```pascal
FUNCTION ConvertHSF2PosixPath(
				HSFPath          : DYNARRAY[] of CHAR;
				VAR outPosixPath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ConvertHSF2PosixPath(HSFPath):
    return (BOOLEAN, outPosixPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|HSFPath|DYNARRAY[] of CHAR|The HSF path that is to be converted.|
|outPosixPath|DYNARRAY[] of CHAR|Output parameter. Returns the converted path. If the function does not succeed the returned value is the passed 'HSFPath' value.|

## Remarks
*_c_* (2016.06.16): This doesn't fail easily (I never could see a failure) but will return gibberish upon anything but a qualified HSF path. Interestingly, passing a qualified posix path (needing thus no conversion!) will also return gibberish:

Example:
 path2convert := Macintosh HD:Users:user:Desktop:New File.txt
 ConvertHSF2PosixPath(path2convert, path)
 --> Macintosh HD:Users:user:Desktop:New File.txt > /Users/user/Desktop/New File.txt
 --> OK

 path2convert := /Users/user/Desktop/New File.txt { <-- this needs no conversion! }
 ConvertHSF2PosixPath(path2convert, path)
 --> /Users/user/Desktop/New File.txt > /:Users:user:Desktop:New File.txt
 --> GIBBERISH

## See Also
VS Functions:
[ConvertPosix2HSFPath](ConvertPosix2HSFPath.md)

## Version
Availability: from Vectorworks 2010

## Category
* [File I@O](../Categories/File%20IO.md)
