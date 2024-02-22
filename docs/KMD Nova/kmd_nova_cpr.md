---
layout: default
title: cpr
parent: kmd_nova
---

## get_address_by_cpr
(cpr: str, nova_access: NovaAccess) -> dict

```
    Gets the street address of a citizen by their CPR number.

    Args:
        cpr: CPR number of the citizen.

    Returns:
        A dict with the address information.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

