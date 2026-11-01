![Banner](banner.png)

# codeintel-API-Schema-Validator
Validates API request and response structures against a JSON Schema definition. An OpenAPI document is rejected with an explanation; pass the JSON Schema object itself instead. Focused on tools for static code analysis, vulnerability scanning, and code quality assurance.

## Install
`git clone https://github.com/ShadowGuard-AI/codeintel-api-schema-validator`

## Usage
`python3 main.py DATA_FILE SCHEMA_FILE [--data_type json|yaml] [--schema_type json|yaml] [--log_level LEVEL]`

## Parameters
- `-h`: Show help message and exit
- `data_file`: Path to the API request/response data file (JSON or YAML). Required.
- `schema_file`: Path to the OpenAPI or schema definition file (JSON or YAML). Required.
- `--data_type`: Specify the data file type (json or yaml). Inferred from extension if omitted.
- `--schema_type`: Specify the schema file type (json or yaml). Inferred from extension if omitted.
- `--log_level`: Set the logging level. Choices: DEBUG, INFO, WARNING, ERROR, CRITICAL. Default: INFO.

## Verified behavior
- Valid data against a matching schema exits 0.
- Data that violates the schema exits 1 with the validation failure.
- A schema file containing an `openapi` or `swagger` key is rejected with exit 1 and the message that a plain JSON Schema must be passed instead.

## License
See LICENSE.
