# GetCurrentMode

## Description
Returns the current application protection mode as bitwise OR.  Each bit is used as a flag to indicate what is allowable in a 16 bit byte.

Return values:

0 - Mode Not Set

1 - Full Mode

2 - Demo Mode

4 - Education Mode

8 - Student Mode

16 - Viewer Mode

32 - Unlicensed Mode

64 - Banner Mode

128 - Watermark New Files Mode

256 - Print Watermark Mode

512 - Save Educational File Format Mode

1024 - Open Educational File Format Mode

2048 - Vector Script Export Mode

4096 - Beta Serial Number Mode


456 in binary is 0000111001000.  (Read from the right to left)

8 Student Mode

64 Banner Mode

128 Watermark New Files Mode

256 Print Watermark Mode

256+128+64+8 = 456

```pascal
FUNCTION GetCurrentMode : INTEGER;
```

```python
def vs.GetCurrentMode():
    return INTEGER
```

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
