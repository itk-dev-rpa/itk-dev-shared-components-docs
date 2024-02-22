---
layout: default
title: authentication
parent: graph
---

## authorize_by_username_password
(username: str, password: str, *, client_id: str, tenant_id: str) -> GraphAccess

```
    Get a bearer token for the given user.
    This is used in most other Graph API calls.

    Args:
        username: The username of the user (email address).
        password: The password of the user.
        client_id: The Graph API client id in 8-4-4-12 format.
        tenant_id: The Graph API tenant id in 8-4-4-12 format.

    Returns:
        GraphAccess: The GraphAccess object used to authorize Graph access.
    
```

