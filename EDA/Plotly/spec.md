in [[subplot]], we need spec

{"type": "xy"} for histogram, boxplot
{"type": "table"} for table 

Subplot type https://plotly.com/python/subplots/

Here are the possible values for the `type` option:

-   `"xy"`: 2D Cartesian subplot type for scatter, bar, etc. This is the default if no `type` is specified.
-   `"scene"`: 3D Cartesian subplot for scatter3d, cone, etc.
-   `"polar"`: Polar subplot for scatterpolar, barpolar, etc.
-   `"ternary"`: Ternary subplot for scatterternary.
-   `"mapbox"`: Mapbox subplot for scattermapbox.
-   `"domain"`: Subplot type for traces that are individually positioned. pie, parcoords, parcats, etc.
-   trace type: A trace type name (e.g. `"bar"`, `"scattergeo"`, `"carpet"`, `"mesh"`, etc.) which will be used to determine the appropriate subplot type for that trace.