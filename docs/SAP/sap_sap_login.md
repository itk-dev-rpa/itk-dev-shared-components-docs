---
layout: default
title: sap_login
parent: sap
---

## login_using_portal
(username:str, password:str)

```
    Open KMD Portal in Edge, login and start SAP GUI.
    Args:
        user: KMD Portal username.
        password: KMD Portal password.
    
```

## login_using_cli
(username: str, password: str, client:str='751', system:str='P02', timeout:int=10) -> None

```
    Open and login to SAP with commandline expressions.
    Args:
        username: AZ username
        password: password
        client: Kommune ID (Aarhus = 751). Defaults to '751'.
        system: Environment SID (e.g. P02 = 'KMD OPUS Produktion [P02]'). Defaults to 'P02'.
        timeout: The time in seconds to wait for SAP Logon to start. Defaults to 10.
    Raises:
        TimeoutError: If SAP doesn't start within timeout limit.
        ValueError: If SAP is unable to log in using the given credentials.
    
```

## change_password
(username:str, old_password:str, new_password:str,
client:str='751',
system:str='...KMD OPUS Produktion [P02]',
timeout:int=10) -> None

```
    Change the password of a user in SAP Gui. Closes SAP when done.
    Args:
        username: The username of the user.
        old_password: The current password of the user.
        new_password: The new password to change to.
        client: The client number. Defaults to '751'.
        system: The description string of the connection as displayed in SAP Logon. Defaults to '...KMD OPUS Produktion [P02]'.
        timeout: The time in seconds to wait for SAP Logon to start. Defaults to 10.
    Raises:
        TimeoutError: If the connection couldn't be established within the timeout limit.
        ValueError: If the current credentials are not valid or if the password can't be changed.
        ValueError: If the new password is not valid.
    
    
```

## kill_sap
()

```
    Kills all SAP processes currently running.
```

