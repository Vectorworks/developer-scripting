# GetVersion

## Description
Returns version information about the VectorWorks application. Parameter major returns the major version number of the application. Parameters minor and maintenance return minor version information. Parameter platform returns the OS platform on which VectorWorks is running (1 = Macintosh, 2 = Windows).

For example:

VectorWorks 8.0.1 running on a Macintosh would return:

major: 8
minor: 0
maintenance: 1
platform: 1

```pascal
PROCEDURE GetVersion(
				VAR major       : INTEGER;
				VAR minor       : INTEGER;
				VAR maintenance : INTEGER;
				VAR platform    : INTEGER);
```

```python
def vs.GetVersion():
    return (major, minor, maintenance, platform)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|major|INTEGER|Returns major version number of application.|
|minor|INTEGER|Returns minor version number of application.|
|maintenance|INTEGER|Returns maintenance version number of application.|
|platform|INTEGER|Returns platform of application.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR 
osMajor, osMinor, osIncr :LONGINT; 
appMajor, appMinor, appMaint, platform :INTEGER;
platformStr :STRING;
BEGIN
GetVersion(appMajor, appMinor, appMaint, platform);
GetOSVersion(osMajor, osMinor, osIncr);
IF (platform = 1) 
THEN platformStr := 'MacOS'
ELSE platformStr := 'Windows';
Message('VectorWorks ', appMajor, '.', appMinor, '.', appMaint, ' running on ', platformStr, ' ', osMajor, '.', osMinor, '.', osIncr);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	appMajor, appMinor, appMaint, platform = vs.GetVersion()
	osMajor, osMinor, osIncr = vs.GetOSVersion()
	if (platform == 1):
		platformStr = 'MacOS'
	else:
		platformStr = 'Windows'
	vs.Message('VectorWorks ', appMajor, '.', appMinor, '.', appMaint, ' running on ', platformStr, ' ', osMajor, '.', osMinor, '.', osIncr)

Example()
```

## Version
Availability: from MiniCAD7.0

## Category
* [Utility](../Categories/Utility.md)
