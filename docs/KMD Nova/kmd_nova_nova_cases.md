---
layout: default
title: nova_cases
parent: kmd_nova
---

## get_cases
(nova_access: NovaAccess, cpr: str = None, case_number: str = None, case_title: str = None, limit: int = 100) -> list[NovaCase]

```
    Search for cases on different search terms.
    Currently supports search on cpr number, case number and case title. At least one search term must be given.

    Args:
        nova_access: The NovaAccess object used to authenticate.
        cpr: The cpr number to search on. E.g. "0123456789"
        case_number: The case number to search on. E.g. "S2022-12345"
        case_title: The case title to search on.
        limit: The maximum number of cases to find (1-500).

    Returns:
        A list of NovaCase objects.

    Raises:
        ValueError: If no search terms are given.
        requests.exceptions.HTTPError: If the request failed.
    
```

## add_case
(case: NovaCase, nova_access: NovaAccess, security_unit_id: int = 818485, security_unit_name: str = "Borgerservice")

```
    Add a case to KMD Nova. The case will be created as 'Active'.

    Args:
        case: The case object describing the case.
        nova_access: The NovaAccess object used to authenticate.
        security_unit_id: The id of the security unit that has access to the case. Defaults to 818485.
        security_unit_name: The name of the security unit that has access to the case. Defaults to "Borgerservice".

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

