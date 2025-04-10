The delete.py has the following component
1. layer = iface.activeLayer(): This line uses the iface object and runs the activeLayer() method 
which returns the currently selected layer in QGIS. The method returns the reference to the 
layer which is saved in the layer variable.
2. layer.startEditing(): This is equivalent to putting the layer in the editing mode.
3. layer.deleteAttribute(1): The deleteAttribute() is a method from QgsVectorLayer class. It 
takes the index of the attribute to be deleted. Here we pass on index 1 for the second 
attribute. (index 0 is the first attribute)
4. layer.commitChanges(): This method saves the edit buffer and also disables the editing 
mode.

Working with Geospatial data can be cumbersome at time, and you may just be wondering how to remove some column of attribute that are unused. PyGIS offers an amazing solution to this. By inserting the image on the QGIS outlook. You can run the above code and then it will be waved away.

**An example**: OSM provide resourceful information that has a number of attributes that may not be of use. To eliminate this you can use QGIS to do that.

**Caution**: The indexing has to be put in place to avoid deleting the wrong attribute. Always remember index “0” as the first attribute.
