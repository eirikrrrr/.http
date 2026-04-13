# .http//

dot//http is a file-driven HTTP request runner backed by curl.

dot//http is designed to make HTTP interactions reproducible, scriptable, and easy to reason about. Instead of relying on GUI clients or ad-hoc curl commands, requests are declared in a clean, human-readable format that closely resembles raw HTTP.

The tool parses these .http files, resolves variables, and executes the request using curl as its underlying engine. This approach leverages curl’s reliability while providing a higher-level, file-based workflow.

Key capabilities include:

Define HTTP/HTTPS requests in simple .http files
Support for headers, body payloads, and standard HTTP methods
Variable interpolation for dynamic values
Execute the same request against multiple targets
CLI-first design for automation and integration into scripts

dot//http focuses on clarity and reproducibility over complexity. It is not a full-featured API client, but a minimal, composable tool for developers who prefer working close to the protocol.


## Development

### Scalffold

```

dothttp/
├── pyproject.toml
├── README.md
├── .gitignore
├── src/
│   └── dothttp/
│       ├── __init__.py
│       ├── cli.py
│       ├── errors.py
│       ├── models.py
│       ├── constants.py
│       ├── parser/
│       │   ├── __init__.py
│       │   ├── http_file.py
│       │   └── variables.py
│       ├── validator/
│       │   ├── __init__.py
│       │   └── request.py
│       ├── executor/
│       │   ├── __init__.py
│       │   ├── curl_builder.py
│       │   ├── runner.py
│       │   └── results.py
│       ├── loaders/
│       │   ├── __init__.py
│       │   └── variable_sets.py
│       └── utils/
│           ├── __init__.py
│           └── text.py
└── tests/
    ├── test_parser.py
    ├── test_renderer.py
    ├── test_validator.py
    ├── test_curl_builder.py
    └── test_runner.py

```