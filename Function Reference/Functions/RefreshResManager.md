# RefreshResManager

## Description
Procedure RefreshResManager updates the Resource manager palette. It refreshes Libraries specified by the parameters.

```pascal
PROCEDURE RefreshResManager(
				updateVWLibs     : BOOLEAN;
				updateUserLibs   : BOOLEAN;
				updateWGLibs     : BOOLEAN;
				updateFavs       : BOOLEAN;
				UpdateOnlineLibs : BOOLEAN);
```

```python
def vs.RefreshResManager(updateVWLibs, updateUserLibs, updateWGLibs, updateFavs, UpdateOnlineLibs):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|updateVWLibs|BOOLEAN|Update Vectorworks libraries.|
|updateUserLibs|BOOLEAN|Update User libraries.|
|updateWGLibs|BOOLEAN|Update Workgroups libraries.|
|updateFavs|BOOLEAN|Update Favorites.|
|UpdateOnlineLibs|BOOLEAN|Update Vectorworks online libraries.|

## Version
Availability: from Vectorworks 2025

## Category
* [Utility](../Categories/Utility.md)
