---
layout: default
title: multi_session
parent: sap
---

## run_with_session
(session_index: int, func: Callable, args: tuple) -> None

```
    Run a function in a specific session based on the sessions index.
    This function is meant to be run inside a separate thread.
    The function must take a session object as its first argument.
    Note that this function will not spawn the sessions before running,
    use spawn_sessions to do that.
    
```

## run_batch
(func: Callable, args: tuple[tuple]) -> None

```
    Run a function in parallel sessions.
    A number of threads equal to the length of args will be spawned.
    The function must take a session object as its first argument.
    Note that this function will not spawn the sessions before running,
    use spawn_sessions to do that.

    Args:
        func: A callable function to run in the threads.
        args: A tuple of tuples containing arguments to be passed to func.

    Raises:
        Exception: Any exception raised in any of the threads.
    
```

## run_batches
(func: Callable, args: tuple[tuple], num_sessions: int = 6) -> None

```
    Run a function in parallel batches.
    This function runs the input function for each set of arguments in args.
    The function will be run in parallel batches of size {num_sessions}.
    The function must take a session object as its first argument.
    Note that this function will not spawn the sessions before running,
    use spawn_sessions to do that.
    
```

## spawn_sessions
(num_sessions=6) -> list

```
    A function to spawn multiple sessions of SAP.
    This function will attempt to spawn the desired number of sessions.
    If the current number of already open sessions exceeds the desired number of sessions
    the already open sessions will not be closed to match the desired number.
    The number of sessions must be between 1 and 6.

    Args:
        num_sessions: The number of sessions desired. Defaults to 6.

    Raises:
        ValueError: If the number of sessions is not between 1 and 6.

    Returns:
        tuple: A tuple of all currently open sessions.
    
```

## get_all_sap_sessions
() -> tuple

```
    Returns a tuple of all open SAP sessions (on connection index 0).

    Returns:
        tuple: A tuple of SAP GuiSession objects.
    
```

## arrange_sessions
()

```
    Take all toplevel windows of currently open SAP sessions
    and arrange them equally on the screen.
    
```

