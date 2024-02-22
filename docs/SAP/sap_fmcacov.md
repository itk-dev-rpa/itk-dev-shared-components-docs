---
layout: default
title: fmcacov
parent: sap
---

## open_forretningspartner
(session, fp: str) -> None

```
    Start the transaction FMCACOV and open the given forretningspartner.
    If the fp-number also matches a cvr-number the fp-number will be opened.

    Args:
        session: The SAP session to perform the action.
        fp: The forretningspartner number.

    Raises:
        ValueError: If the forretningspartner wasn't found.
    
```

## dismiss_key_popup
(session, fp: str = "25564617") -> None

```
    Once a day a popup appears asking to generate a new "afstemningsnøgle".
    This function forces it to appear and clicks "Ja" on it.
    This is done by pretending to do "Kontovedligehold" on the given forretningspartner.
    The function should start and end at the home screen.

    Args:
        session: The SAP session object.
        fp: The forretningspartner to used. Defaults to "25564617" a fictional person in AAK.

    Raises:
        RuntimeError: If a popup other than the expected ones appear.
    
```

