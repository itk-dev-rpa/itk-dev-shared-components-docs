---
layout: default
title: nova_tasks
parent: kmd_nova
---

## attach_task_to_case
(case_uuid: str, task: Task, nova_access: NovaAccess) -> None

```
    Attach a Task object to a case in Nova.

    The Task object must have the following values set:
    uuid, title, status_code, deadline, case_worker_uuid.

    Args:
        case_uuid: The id of the case to attach the task to.
        task: A Task object describing the task.
        nova_access: The NovaAccess object used to authenticate.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

## get_tasks
(case_uuid: str, nova_access: NovaAccess, limit: int = 100) -> list[Task]

```
    Get tasks attached to a case.

    Args:
        case_uuid: The id of the case.
        nova_access: The NovaAccess object used to authenticate.
        limit: The max number of tasks to get. Defaults to 100.

    Returns:
        A list of Task objects.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

## update_task
(task: Task, case_uuid: str, nova_access: NovaAccess)

```
    Update a task that already exists in KMD Nova with new
    information.

    Args:
        task: The Task object describing the updated task.
        case_uuid: The id of the case the task belongs to.
        nova_access: The NovaAccess object used to authenticate.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

