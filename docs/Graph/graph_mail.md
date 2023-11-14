---
layout: default
title: mail
parent: graph
---

## get_emails_from_folder
(user: str, folder_path: str, graph_access: GraphAccess) -> tuple[Email]

```
    Get all emails from the specified user and folder.
    You need to authorize against Graph to get the GraphAccess before using this function
    see the graph.authentication module.

    Args:
        user: The user who owns the folder.
        folder_path: The absolute path of the folder e.g. 'Inbox/Economy/May'
        graph_access: The GraphAccess object used to authenticate.

    Returns:
        tuple[Email]: The emails from the given folder.
    
```

## get_email_as_mime
(email: Email, graph_access: GraphAccess) -> io.BytesIO

```
    Get an email as a file-like object in MIME format.

    Args:
        email: The email to get as MIME.
        graph_access: The GraphAccess object used to authenticate.

    Returns:
        io.BytesIO: A file-like object of the MIME file.
    
```

## get_folder_id_from_path
(user: str, folder_path: str, graph_access: GraphAccess) -> str

```
    Get the Graph id of a folder based on the path of the folder.
    You need to authorize against Graph to get the GraphAccess before using this function
    see the graph.authentication module.

    Args:
        user: The user who owns the folder.
        folder_path: The absolute path of the folder e.g. 'Inbox/Economy/May'
        graph_access: The GraphAccess object used to authenticate.

    Raises:
        ValueError: If a folder in the path can't be found.

    Returns:
        str: The UUID of the folder in Graph.
    
```

## list_email_attachments
(email: Email, graph_access: GraphAccess) -> tuple[Attachment]

```
    List all attachments of the given email. This function only gets the id, name and size
    of the attachment. Use get_attachment_data to get the actual data of an attachment.

    Args:
        email: The email which attachments to list.
        graph_access: The GraphAccess object used to authenticate.

    Returns:
        tuple[Attachment]: A tuple of Attachment objects describing the attachments.
    
```

## get_attachment_data
(attachment: Attachment, graph_access: GraphAccess) -> io.BytesIO

```
    Get a file-like object representing the attachment.

    Args:
        attachment: The attachment to get.
        graph_access: The GraphAccess object used to authenticate.

    Returns:
        io.BytesIO: A file-like object representing the attachment.
    
```

## move_email
(email: Email, folder_path: str, graph_access: GraphAccess, *, well_known_folder: bool=False) -> None

```
    Move an email to another folder under the same user.
    If well_known_folder is true, the folder path is assumed to be a well defined folder.
    See https://learn.microsoft.com/en-us/graph/api/resources/mailfolder?view=graph-rest-1.0 
    for a list of well defined folder names.

    Args:
        email: The email to move.
        folder_path: The absolute path to the new folder. E.g. 'Inbox/Economy/May'
        graph_access: The GraphAccess object used to authenticate.
        well_known_folder: Whether the path is a 'well known folder'. Defaults to False.
    
```

## delete_email
(email: Email, graph_access: GraphAccess, *, permanent: bool=False) -> None

```
    Delete an email from the mailbox.
    If permanent is true the email is completely removed from the user's mailbox.
    If permanent is false the email is instead moved to the Deleted Items folder.

    Args:
        email: The email to delete.
        graph_access: The GraphAccess object used to authenticate.
        permanent: Whether to permanently remove the email or not. Defaults to False.
    
```

