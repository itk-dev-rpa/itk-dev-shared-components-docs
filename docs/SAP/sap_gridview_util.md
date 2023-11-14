---
layout: default
title: gridview_util
parent: sap
---

## scroll_entire_table
(grid_view, return_to_top=False) -> None

```
    This function scrolls through the entire table to load all cells.

    Args:
        grid_view: A SAP GuiGridView object.
        return_to_top: Whether to return the table to the first row after scrolling. Defaults to False.
    
```

## get_all_rows
(grid_view, pre_load=True) -> tuple[tuple[str]]

```
    Get all values from a table and return them in a 2D tuple.

    Args:
        grid_view: A SAP GuiGridView object.
        pre_load: Whether to first scroll through the table to load all values.
                  If a row hasn't been loaded before reading, the row data will be empty. 

    Returns:
        tuple[tuple[str]]: A 2D tuple of all cell values in the gridview.
    
```

## get_row
(grid_view, row:int, scroll_to_row=False) -> tuple[str]

```
    Returns the data of a single row.

    Args:
        grid_view: A SAP GuiGridView object.
        row: The zero-based index of the row.
        scroll_to_row: Whether to scroll to the row before reading the data.
                       This ensures the data of the row has been loaded before reading. 

    Returns:
        tuple[str]: A tuple of the row's data.
    
```

## iterate_rows
(grid_view) -> tuple[str]

```
    This generator yields each row of the table in order.
    This is preferable to loading all rows as this will only load a row when it's needed.
    As a side effect this function scrolls the yielded row into view, so the
    table doesn't need to be pre-loaded before calling this function.

    Args:
        grid_view: A SAP GuiGridView object.

    Yields:
        tuple[str]: A tuple of the next row's data.
    
```

## get_column_titles
(grid_view) -> tuple[str]

```
    Get the column titles of the table instead of the column ids.
    To get the column ids use grid_view.ColumnOrder.

    Args:
        grid_view: A SAP GuiGridView object.

    Returns:
        tuple[str]: A tuple of the gridview's column titles.
    
```

## find_row_index_by_value
(grid_view, column:str, value:str) -> int

```
    Find the index of the first row where the given column's value
    matches the given value. Returns -1 if no row is found.

    Args:
        grid_view: A SAP GuiGridView object.
        column: The id of the column.
        value: The value to search for.

    Raises:
        ValueError: If the gridview doesn't contain a column with the given id.

    Returns:
        int: The index of the first row which column value matches the given value.
    
```

## find_all_row_indices_by_value
(grid_view, column:str, value:str) -> list[int]

```
    Find all indices of the rows where the given column's value
    match the given value. Returns an empty list if no row is found.

    Args:
        grid_view (_type_): A SAP GuiGridView object.
        column (str): The name of the column whose value to check.
        value (str): The value to search for.

    Raises:
        ValueError: If the column name doesn't exist in the grid view.

    Returns:
        list[int]: A list of row indices where the value matches.
    
```

