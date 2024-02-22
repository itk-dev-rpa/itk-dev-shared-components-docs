---
layout: default
title: tree_util
parent: sap
---

## get_node_key_by_text
(tree, text: str, fuzzy: bool = False) -> str

```
    Get the node key of a node based on its text.

    Args:
        tree: A SAP GuiTree object.
        text: The text to search for.
        fuzzy: Whether to check if the node text just contains the search text.

    Raises:
        ValueError: If no node is found with the given text.

    Returns:
        str: The node key of the found node.
    
```

## get_item_by_text
(tree, text: str, fuzzy: bool = False) -> tuple[str, str]

```
    Get the node key and item name of an item based on its text.

    Args:
        tree: A SAP GuiTree object.
        text: The text to search for.
        fuzzy: Whether to check if the item text just contains the search text.

    Raises:
        ValueError: If no tem is found with the given text.

    Returns:
        tuple[str,str]: The node key and item name of the found item.
    
```

## check_all_check_boxes
(tree) -> None

```
    Find and check all checkboxes in the tree.

    Args:
        tree: A SAP GuiTree object.
    
```

## uncheck_all_check_boxes
(tree) -> None

```
    Find and uncheck all checkboxes in the tree.

    Args:
        tree: A SAP GuiTree object.
    
```

