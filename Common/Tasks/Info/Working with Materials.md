# MaterialProperty

Most fields of the BuildingMaterial resource use selectors which are shown in the tables below.
The MATERIALPROPERTY worksheet function uses text selectors that can be universal or localized. The text selectors shown are the universal names (which are also the English localized names).
SDK and VectorScript can use the numbers shown as Object Variable selectors (e.g. gSDK->GetObjectVariable or VS GetObjectVariableString/GetObjectVariableReal/GetObjectVariableBoolean).

## MaterialProperty values

### General info fields are (text)

| **Text Selector** | **ov Constant** | **ov value** |
|-------------------|-----------------|--------------|
| MaterialDescription | ovMaterialDescription | 1606 |
| MaterialKeynote | ovMaterialKeynote | 1608 |
| MaterialMark | ovMaterialMark | 1607 |

### Physical values are (real), but they also have an associated (bool) that indicates whether they are populated or not, so the material can show the field as zero vs blank.

| **Text Selector** | **ov Constant** | **ov value** | **Text Selector** | **ov Constant** | **ov value** |
|-------------------|-----------------|--------------|-------------------|-----------------|--------------|
| MaterialAcousticImpedance | ovMaterialAcousticImpedance | 1591 | MaterialUsesAcousticImpedance | ovMaterialUsesAcousticImpedance | 1604 |
| MaterialAlbedo | ovMaterialAlbedo | 1585 | MaterialUsesAlbedo | ovMaterialUsesAlbedo | 1598 |
| MaterialDensity | ovMaterialDensity | 1590 | MaterialUsesDensity | ovMaterialUsesDensity | 1603 |
| MaterialEmbodiedCarbon | ovMaterialEmbodiedCarbon | 1588 | MaterialUsesEmbodiedCarbon | ovMaterialUsesEmbodiedCarbon | 1601 |
| MaterialEmissivity | ovMaterialEmissivity | 1584 | MaterialUsesEmissivity | ovMaterialUsesEmissivity | 1597 |
| MaterialLambda | ovMaterialLambda | 1587 | MaterialUsesLambda | ovMaterialUsesLambda | 1600 |
| MaterialModulusOfElasticity | ovMaterialModulusOfElasticity | 1580 | MaterialUsesModulusOfElasticity | ovMaterialUsesModulusOfElasticity | 1593 |
| MaterialSlipResistance | ovMaterialSlipResistance | 1612 | MaterialUsesSlipResistance | ovMaterialUsesSlipResistance | 1613 |
| MaterialSoundVelocity | ovMaterialSoundVelocity | 1589 | MaterialUsesSoundVelocity | ovMaterialUsesSoundVelocity | 1602 |
| MaterialSpecificGravity | ovMaterialSpecificGravity | 1579 | MaterialUsesSpecificGravity | ovMaterialUsesSpecificGravity | 1592 |
| MaterialSpecificHeat | ovMaterialSpecificHeat | 1583 | MaterialUsesSpecificHeat | ovMaterialUsesSpecificHeat | 1596 |
| MaterialTensileStrength | ovMaterialTensileStrength | 1582 | MaterialUsesTensileStrength | ovMaterialUsesTensileStrength | 1595 |
| MaterialThermalExpansionCoefficient | ovMaterialThermalExpansionCoefficient | 1586 | MaterialUsesThermalExpansionCoefficient | ovMaterialUsesThermalExpansionCoefficient | 1599 |
| MaterialYieldStrength | ovMaterialYieldStrength | 1581 | MaterialUsesYieldStrength | ovMaterialUsesYieldStrength | 1594 |

### Construction info are (text), except Cost is a (real)

| **Text Selector** | **ov Constant** | **ov value** |
|-------------------|-----------------|--------------|
| MaterialCategory | ovMaterialCategory | 1570 |
| MaterialClassificationDescription | ovMaterialClassificationDescription | 1573 |
| MaterialCost | ovMaterialCost | 1609 |
| MaterialFinish | ovMaterialFinish | 1611 |
| MaterialIsSurfaceAreaMeasure | ovMaterialIsSurfaceAreaMeasure | 1605 |
| MaterialIsVolumetric | ovMaterialIsVolumetric | 1569 |
| MaterialManufacturer | ovMaterialManufacturer | 1574 |
| MaterialProductDescription | ovMaterialProductDescription | 1577 |
| MaterialProductModel | ovMaterialProductModel | 1575 |
| MaterialProductName | ovMaterialProductName | 1576 |
| MaterialProductURL | ovMaterialProductURL | 1578 |
| MaterialReferenceID | ovMaterialReferenceID | 1572 |
| MaterialSource | ovMaterialSource | 1610 |
| MaterialStandard | ovMaterialStandard | 1571 |
