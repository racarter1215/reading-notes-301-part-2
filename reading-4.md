# Grids

##### grid-column-start: 3; will water the area starting at the 3rd vertical grid line, which is another way of saying the 3rd vertical border from the left in the grid.

##### Grid column start selects which grid square you start modifying at.

##### When grid-column-start is used alone, the grid item by default will span exactly one column. However, you can extend the item across multiple columns by adding the grid-column-end property

##### When pairing grid-column-start and grid-column-end, you might assume that the end value has to be greater than the start value. But this turns out not the case!

##### If you want to count grid lines from the right instead of the left, you can give grid-column-start and grid-column-end negative values. For example, you can set it to -1 to specify the first grid line from the right.

##### Grid column can be set to a negative value

##### Instead of defining a grid item based on the start and end positions of the grid lines, you can define it based on your desired column width using the span keyword. Keep in mind that span only works with positive values.

##### You can also use the span keyword with grid-column-start to set your item's width relative to the end position.


