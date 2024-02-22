---
layout: default
title: cpr_util
parent: misc
---

## get_age
(cpr: str, current_date: date = date.today()) -> int

```
    Get the age of a person based on their cpr number
    using the 7th digit to infer the century.

    Args:
        cpr: The cpr number in the format 'ddmmyyxxxx'.
        current_date: The date where the age is calculated from. Defaults to the current date.

    Returns:
        The age in integer years based on the cpr number.

    Raises:
        ValueError: If the given cpr is not in 'ddmmyyxxxx' format.
    
```

