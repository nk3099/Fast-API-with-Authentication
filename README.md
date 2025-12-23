### In FastAPI:
Decorator line (the route definition) declares what the endpoint returns (the response) and static metadata like status code.
Function signature declares what the endpoint receives (the request inputs)—body, path/query params, and injected dependencies.

### What is Depends?
Depends is part of FastAPI’s dependency system.
It tells FastAPI: “Run this function before the endpoint and inject its return value into my parameter.”

### In Networking:
A host is any device (computer, server, IoT device) that has an IP address and can communicate over a network.
In a connection, the host is typically the endpoint you are connecting to or from.


### Serialization:
- FastAPI automatically serializes your return values (dict, Pydantic model) into JSON for HTTP responses.

- Serialization means converting an object (like a Python dictionary, class instance, or data structure) 
into a format that can be easily stored or transmitted (e.g., JSON, XML, or binary). The reverse process is called deserialization.

- <u> Common Use Case in Python </u>
  - APIs: When sending data over HTTP, you serialize Python objects to JSON.
  - Databases: Store structured data as strings or blobs.
  - Caching: Save objects in Redis or files.

Example:
```

import json

data = {"id": 1, "title": "Hello", "tags": ["python", "fastapi"]}

# Serialize (Python object → JSON string)
json_string = json.dumps(data)
print(json_string)  # {"id": 1, "title": "Hello", "tags": ["python", "fastapi"]}

# Deserialize (JSON string → Python object)
parsed_data = json.loads(json_string)
print(parsed_data["title"])  # Hello

```



