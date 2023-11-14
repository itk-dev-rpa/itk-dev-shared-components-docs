---
layout: default
title: opret_kundekontakt
parent: sap
---

## opret_kundekontakter
(session, fp:str, aftaler:list[str] | None,
art:Literal[' ', 'Automatisk', 'Fakturagrundlag', 'Fuldmagt ifm. værge', 'Konverteret', 'Myndighedshenvend.', 'Orientering', 'Returpost', 'Ringeaktivitet', 'Skriftlig henvend.', 'Telefonisk henvend.'],
notat:str, lock=None) -> None

```
    Creates a kundekontakt on the given FP and aftaler.

    Args:
        session (COM Object): The SAP session to preform the action.
        fp (str): The forretningspartner number.
        aftaler (list[str] | None): A list of aftaler to put the kundekontakt on. If empty or None the kundekontakt will be created on fp-level.
        art (str): The art of the kundekontakt.
        notat (str): The text of the kundekontakt.
        lock (threading.Lock, optional): A threading.Lock object to allow this function to run properly when multithreaded. Defaults to None.
    
```

