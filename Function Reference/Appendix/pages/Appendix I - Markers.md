# Appendix I - Markers

## Marker Styles and Constants

A marker style constant can be created by combining some of the basic elements listed below (Root Type, Base, Fill, Half Tick and Tail).

| Root Type | Constant |
|-----------|----------|
| Arrow Marker | 0 |
| ConcavedCurvedArrowMarker | 1 |
| CircleMarker | 2 |
| DimSlashMarker | 3 |
| DimCrossMarker | 4 |
| LassoMarker | 5 |
| HexagonMarker | 6 |
| VShapedMarker | 7 |
| ConeShapedMarker | 8 |
| TaperedVShapedMarker | 9 |
| SShapedMarker | 10 |
| RectangleMarker | 11 |
| DoubleLineMarker | 12 |

| Base (Only meaningful for ArrowMarker and ConcaveCurvedArrowMarker) | Constant |
|---------------------------------------------------------------|----------|
| FlatBaseMarker |  |
| OpenBaseMarker | 1024 |
| AngleBaseMarker | 2048 |
| ArcBaseMarker | 3072 |

| Fill | Constant |
|------|----------|
| LineColorMarker | 0 |
| WhiteFillMarker | 128 |
| NoFillMarker | 256 |

**Note**: NoFillMarker is the only valid setting for LassoMarker, DimSlashMarker, and DimCrossMarker.

| Tail (Meaningless for CircleMarker, DimCrossMarker, LassoMarker, HexagonMarker, ConeMarker, and RectangleMarker) | Constant |
|---------------------------------------------------------------------------------------------------------------|----------|
| TailMarker | 32768 |

| Half Tick (Meaningless for LassoMarker and ConeMarker) | Constant |
|--------------------------------------------------------|----------|
| LeftHalfTickMarker | 16384 |
| RightHalfTickMarker | 24576 |

| Useful Composite Constants (Use these instead of Simple Constants) | Constant |
|-------------------------------------------------------------------|----------|
| OpenBaseNoFillMarker | 128 |
| NoFillLassoMarker | 261 |
| NoFillDimSlashMarker | 259 |
| NoFillConeMarker | 264 |
| WhiteFillConeMarker | 136 |

| Examples | Constant |
|----------|----------|
| ![Example 1](images/Vs_appendix_clip_image002_0001.jpg) | style = 2176 <=> 0 + 2048 + 128 (ArrowMarker + AngleBaseMarker + WhiteFillMarker) |
| ![Example 2](images/Vs_appendix_clip_image002_0002.jpg) | style = 16390 <=> 6 + 0 + 16384 (HexagonMarker + LineColorFillMarker + LeftHalfTickMarker) |

## Marker Thickness Basis and Unit

The marker thickness basis constant specifies the type and unit of the marker thickness to be set.
A marker thickness basis constant is created by adding the thickness unit to the thickness basis. Note that the thickness value and unit are only meaningful for custom thickness.

| Marker Thickness Basis | Constant |
|------------------------|----------|
| Use Line Thickness | 0 |
| Use Dim Thickness | 1 |
| Custom Thickness | 2 |

| Marker Thickness Unit | Constant |
|-----------------------|----------|
| Mils | 0 |
| Points | 16 |
| Millimeters | 32 |

**Examples**:

```
thicknessBasis = 34 <=> 2 + 32 (Custom thickness in Millimeters)
thicknessBasis = 18 <=> 2 + 16 (Custom thickness in Points)
```

**Examples of Marker Styles**:

| Marker Style | Example |
|--------------|---------|
| 0 | ![Example](images/Vs_appendix_clip_image002.jpg) |
| 256 | ![Example](images/Vs_appendix_clip_image004.jpg) |
| 1280 | ![Example](images/Vs_appendix_clip_image005.jpg) |
| 2 | ![Example](images/Vs_appendix_clip_image007.jpg) |
| 130 | ![Example](images/Vs_appendix_clip_image009.jpg) |
| 259 | ![Example](images/Vs_appendix_clip_image011.jpg) |
| 260 | ![Example](images/Vs_appendix_clip_image012.jpg) |
| 2048 | ![Example](images/Vs_appendix_clip_image014.jpg) |
| 17664 | ![Example](images/Vs_appendix_clip_image015.jpg) |
| 261 | ![Example](images/Vs_appendix_clip_image017.jpg) |
| 3073 | ![Example](images/Vs_appendix_clip_image019.jpg) |
| 1281 | ![Example](images/Vs_appendix_clip_image020.jpg) |
| 264 | ![Example](images/Vs_appendix_clip_image022.jpg) |
| 34048 | ![Example](images/Vs_appendix_clip_image024.jpg) |
| 16512 | ![Example](images/Vs_appendix_clip_image025.jpg) |
| 16384 | ![Example](images/Vs_appendix_clip_image027.jpg) |
| 9 | ![Example](images/Vs_appendix_clip_image029.jpg) |
| 135 | ![Example](images/Vs_appendix_clip_image030.jpg) |
| 32903 | ![Example](images/Vs_appendix_clip_image032.jpg) |
| 266 | ![Example](images/Vs_appendix_clip_image033.jpg) |
| 6 | ![Example](images/Vs_appendix_clip_image035.jpg) |
| 128 | ![Example](images/Vs_appendix_clip_image037.jpg) |
