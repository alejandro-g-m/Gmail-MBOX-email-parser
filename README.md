# Gmail MBOX email parser (Python)

## Description

This is a quick solution to parse a Gmail export in MBOX format.

This parsing has been created to process emails for Machine Learning Classification. Therefore, the goal is to create a CSV file with two columns: the email's body and the classification label of that email.

## Usage

By running the file as \_\_main\_\_ it will extract the messages contained in a MBOX file and create a list of _CustomMessage_ objects (_messages_ property).

A _CustomMessage_ contains the __subject__, __body__ and __content type__ of an extracted email.

The code includes several functions used to prepare the extracted data for Machine Learning algorithms that may not be relevant for every use case.

By running this code, after the main processing, the extrated data will be exported to a file:
```python
to_file(text_messages_to_string(messages), 'file_name')
```

## Status

At the time of writing this code I could not find good working examples to do this task. This is why I have decided to upload the developed code, so it can be used as a reference for anybody working on similar tasks. However, this code may not consider many corner cases and most likely will need some modifications depending on the use case. Also, it has not been tested properly yet.

This was developed to serve as a quick solution for a concrete use case that we had to handle in a Machine Learning task, so it should not be considered as a generic way to extract emails from an MBOX file. This has been only tested with Gmail exports, it is unknown how it would work exports from other services.
