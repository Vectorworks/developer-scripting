# ConvertPosix2HSFPath

## Description
MacIntosh only!

Converts Posix (using '/' as delimiter) file path to HSF (using ':' as delimiter) file path.

```pascal
FUNCTION ConvertPosix2HSFPath(
				PosixPath      : DYNARRAY[] of CHAR;
				VAR outHSFPath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.ConvertPosix2HSFPath(PosixPath):
    return (BOOLEAN, outHSFPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|PosixPath|DYNARRAY[] of CHAR|The Posix path that is to be converted.|
|outHSFPath|DYNARRAY[] of CHAR|Output parameter. Returns the converted path. If the function does not succeed the returned value is the passed 'PosixPath' value.|

## Remarks
*\_c\_* (2016.06.16): This doesn't fail easily (I never could see a failure) but will return gibberish upon anything but a qualified Posix path. Interestingly, passing a qualified HSF path (needing thus no conversion!) will also return gibberish:

Example:
 path2convert := /Users/user/Desktop/New File.txt 
 ConvertPosix2HSFPath(path2convert, path)
 --> /Users/user/Desktop/New File.txt > Macintosh HD:Users:user:Desktop:New File.txt
 --> OK

 path2convert := Macintosh HD:Users:user:Desktop:New File.txt { <-- this needs no conversion! }
 ConvertPosix2HSFPath(path2convert, path)
 --> Macintosh HD:Users:user:Desktop:New File.txt > :Macintosh HD/Users/user/Desktop/New File.txt
 --> GIBBERISH

## See Also
VS Functions:
[ConvertHSF2PosixPath](ConvertHSF2PosixPath.md)

## Version
Availability: from Vectorworks 2010

## Category
* [File I@O](../Categories/File%20IO.md)
