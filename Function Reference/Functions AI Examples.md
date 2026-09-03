# Functions AI Examples

This collection provides progressively more advanced Vectorworks Python examples.

These examples are generated using AI analysing internal information.

## Drawing and Document Basics

| Example | Description |
| --- | --- |
| [01. Draw a Room with Walls](Functions/ai%20examples/01_DrawRoomWithWalls.md) | Creates a four-wall rectangular room and applies consistent wall heights. |
| [02. Draw 2D Geometry Primitives](Functions/ai%20examples/02_Draw2DPrimitives.md) | Draws primitive shapes with varied pen and fill attributes. |
| [03. Build a Curved Path with Mixed Vertex Types](Functions/ai%20examples/03_CurvedPolylinePath.md) | Compares straight and rounded polylines built from corner, radius, and arc vertices. |
| [04. Extrude 2D Shapes into 3D Solids](Functions/ai%20examples/04_ExtrudeShapesTo3D.md) | Turns rectangles, ovals, and polygons into positioned 3D extrudes. |
| [05. Turn a Column Profile with Sweep](Functions/ai%20examples/05_SweepColumnAndTorus.md) | Sweeps a stepped profile into a column and adds a torus base. |
| [06. Boolean Solids: Drill a Hole Through a Block](Functions/ai%20examples/06_BooleanSolids.md) | Builds an extruded block, subtracts a cylindrical hole, and adds a top box. |
| [07. Set Up Document Structure: Layers and Classes](Functions/ai%20examples/07_LayersAndClasses.md) | Creates architectural layers and classes with distinct graphic attributes. |
| [08. Attach and Read Records on Objects](Functions/ai%20examples/08_AttachAndReadRecords.md) | Creates a record, attaches it to sample furniture, and reads the stored fields. |
| [09. Dimensioning and Text Annotation](Functions/ai%20examples/09_DimensionsAndText.md) | Produces a measured room drawing with loci, callouts, and linear dimensions. |
| [10. Iterate the Drawing and Report a Summary](Functions/ai%20examples/10_IterateAndReport.md) | Counts active-layer objects and totals bounding-box area using two traversal approaches. |

## Geometry Algorithms

| Example | Description |
| --- | --- |
| [11. 2D Vector Math Toolkit](Functions/ai%20examples/11_VectorMathToolkit.md) | Provides reusable tuple-based 2D vector helpers and visualizes their results. |
| [12. Polygon Area and Centroid (Shoelace Formula)](Functions/ai%20examples/12_PolygonAreaCentroid.md) | Calculates signed polygon area, winding direction, and centroid. |
| [13. Point-in-Polygon Test (Ray Casting)](Functions/ai%20examples/13_PointInPolygonRayCast.md) | Classifies test points inside an arbitrary polygon with ray casting. |
| [14. Polygon Inward / Outward Offset](Functions/ai%20examples/14_PolygonInwardOffset.md) | Rebuilds a polygon after offsetting each edge by a signed distance. |
| [15. Uniform Arc-Length Resampling of a Polyline](Functions/ai%20examples/15_PolylineResampleUniform.md) | Resamples an open polyline into evenly spaced points along its length. |
| [16. Polyline Simplification (Douglas-Peucker)](Functions/ai%20examples/16_DouglasPeuckerSimplify.md) | Reduces a dense polyline while preserving its overall shape. |
| [17. Convex Hull (Andrew's Monotone Chain)](Functions/ai%20examples/17_ConvexHullMonotoneChain.md) | Finds and draws the counter-clockwise convex hull of a point cloud. |
| [18. Line-Segment Intersection Finder](Functions/ai%20examples/18_LineSegmentIntersections.md) | Finds crossings among line segments and marks their intersection points. |
| [19. Cubic Bezier Sampled to a Polyline](Functions/ai%20examples/19_BezierPolylineSampling.md) | Approximates cubic Bezier curves as Vectorworks polylines. |
| [20. Read a Polyline and Build Walls Along Its Path](Functions/ai%20examples/20_PolylineToWalls.md) | Converts a selected or fallback path into auto-mitered, consistently sized walls. |

## Worksheets and Reporting

| Example | Description |
| --- | --- |
| [21. Hello Worksheet — Create and Populate](Functions/ai%20examples/21_WorksheetBasic.md) | Creates, fills, recalculates, and displays a minimal worksheet. |
| [22. Selected Objects → Worksheet Rows](Functions/ai%20examples/22_WorksheetSelectedObjects.md) | Writes selected objects' properties to individual worksheet rows. |
| [23. Count Objects by Criteria (Formula-Driven)](Functions/ai%20examples/23_WorksheetCountByCriteria.md) | Builds a live worksheet dashboard using `COUNT` criteria formulas. |
| [24. Auto-Populating Database Row](Functions/ai%20examples/24_WorksheetDBRowAutoPopulate.md) | Uses a database row and record-field formulas to schedule matching objects automatically. |
| [25. Geometric Property Extraction Table](Functions/ai%20examples/25_WorksheetPolyGeometry.md) | Reports polygon and polyline geometry in a formatted worksheet. |
| [26. Sorting and Grouping with `SetWSColumnOperators`](Functions/ai%20examples/26_WorksheetSortAndGroup.md) | Sorts and summarizes a database-row schedule by worksheet columns. |
| [27. Formatted Wall Schedule](Functions/ai%20examples/27_WorksheetFormattedSchedule.md) | Produces a polished wall schedule with geometry, units, and table formatting. |
| [28. Symbol Instance Schedule](Functions/ai%20examples/28_WorksheetSymbolSchedule.md) | Lists symbol definitions with live instance counts and optional cost totals. |
| [29. Cross-Layer Summary](Functions/ai%20examples/29_WorksheetCrossLayerSummary.md) | Summarizes object and wall metrics across every design layer. |
| [30. Publish Worksheet Image on a Sheet Layer](Functions/ai%20examples/30_WorksheetPublishOnSheet.md) | Builds a printable sheet-layer worksheet image through an idempotent reporting pipeline. |
