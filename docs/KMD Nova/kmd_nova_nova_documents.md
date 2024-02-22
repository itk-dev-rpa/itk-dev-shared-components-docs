---
layout: default
title: nova_documents
parent: kmd_nova
---

## get_documents
(case_uuid: str, nova_access: NovaAccess) -> list[Document]

```
    Get all documents attached to the given case.
    To get the actual document file use download_document_file.

    Args:
        case_uuid: The uuid of the case to get documents from.
        nova_access: The NovaAccess object used to authenticate.

    Returns:
        A list of Document objects describing the documents.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

## download_document_file
(document_uuid: str, nova_access: NovaAccess, checkout: bool = False, checkout_comment: str = None) -> bytes

```
    Download the file attached to a KMD Nova Document.

    Args:
        document_uuid: The uuid of the Nova document.
        nova_access: The NovaAccess object used to authenticate.
        checkout: Whether to mark the document as checked out. Defaults to False.
        checkout_comment: A comment to the checkout. Defaults to None.

    Returns:
        The document file as raw bytes.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

## upload_document
(file: BinaryIO, file_name: str, nova_access: NovaAccess) -> str

```
    Upload a document to Nova. This only uploads the document file.
    To attach the document to a case use attach_document_to_case after calling this.
    The uuid returned should be used to create a new Document object.

    Args:
        file: The file to upload as a file-like object in binary mode.
        file_name: The name of the file including the file extension.
        nova_access: The NovaAccess object used to authenticate.

    Returns:
        The uuid identifying the document in Nova.

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

## attach_document_to_case
(case_uuid: str, document: Document, nova_access: NovaAccess, security_unit_id: int = 818485, security_unit_name: str = "Borgerservice") -> None

```
    Attach a document to a case in Nova.
    The document file first needs to be uploaded using upload_document,
    which also creates the document uuid.

    Args:
        case_uuid: The uuid of the case to attach the document to.
        document: The document object to attach to the case.
        nova_access: The NovaAccess object used to authenticate.
        security_unit_id: The id of the security unit that has access to the document. Defaults to 818485.
        security_unit_name: The name of the security unit that has access to the document. Defaults to "Borgerservice".

    Raises:
        requests.exceptions.HTTPError: If the request failed.
    
```

