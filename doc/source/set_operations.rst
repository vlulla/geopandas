.. ipython:: python
   :suppress:

   import geopandas as gpd


Set-Operations with Overlay
============================

When working with multiple spatial datasets -- especially multiple *polygon* or *line* datasets -- users often wish to create new shapes based on places where those datasets overlap (or don't overlap). These manipulations are often referred using the language of sets -- intersections, unions, and differences. These types of operations are made available in the *geopandas* library through the ``overlay`` function.

The basic idea is demonstrated by the graphic below but keep in mind that overlays operate at the DataFrame level, not on individual geometries, and the properties from both are retained. In effect, for every shape in the first GeoDataFrame, this operation is executed against every other shape in the other GeoDataFrame:

.. image:: _static/overlay_operations.png

**Source: QGIS Documentation**

(Note to users familiar with the *shapely* library: ``overlay`` can be thought of as offering versions of the standard *shapely* set-operations that deal with the complexities of applying set operations to two *GeoSeries*. The standard *shapely* set-operations are also available as ``GeoSeries`` methods.)



.. toctree::
   :maxdepth: 2
