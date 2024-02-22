---
layout: default
title: util
parent: kmd_nova
---

## datetime_from_iso_string
(date_string: Optional[str]) -> Optional[datetime]

```
    A helper function to convert an ISO date string to a datetime.
    If the date string is None, None is returned.

    Args:
        date_string: A date string in ISO format.

    Returns:
        A datetime object representing the date string.
    
```

## datetime_to_iso_string
(datetime_: Optional[datetime]) -> Optional[str]

```
    A helper function to convert a datetime to an ISO formatted string.
    If the the datetime is None, None is returned.

    Args:
        datetime_: The datetime object to convert.

    Returns:
        A datetime string in ISO format.
    
```

