![The lure bulb huge and close in black water, gold against abyss indigo, its stalk arcing away below the frame, silt motes in its radiance, tube worm clusters at the rim of the light, no lettering anywhere](intro-banner.png)


# codeintel-API-Schema-Validator

![An anglerfish entire in profile crossing the midnight zone, lure swaying ahead of its teeth, its gold pool falling on tube worm clusters on the trench floor, and codeintel-api-schema-validator scored into the trench wall in bone white with a gold shadow](banner.png)

![One gold anglerfish lure sphere on a short curved stalk over abyss indigo, dim tube worm clusters at the trench floor, and the name underneath in bone white, the heading plate](logo.png)

![The trench in three depths: silt motes drift and settle in far black water, an anglerfish crosses slowly in the middle depth with its lure swinging in a shallow arc and its glow brightening on the turn while tube worms sway a fraction, and one large tube worm cluster in the near foreground opens and closes its bone white tips slowly, then holds](scene.svg)

Validates API request and response structures against a JSON Schema definition. An OpenAPI document is rejected with an explanation; pass the JSON Schema object itself instead. Focused on tools for static code analysis, vulnerability scanning, and code quality assurance.

![Major separator: a run of small separate bubbles in silt grey across the full width](sep-heavy.svg)

## Install
`git clone https://github.com/ShadowGuard-AI/codeintel-api-schema-validator`

> **Silt ledge: a field, not a behaviour.** The opening above closes with the sentence: Focused on tools for static code analysis, vulnerability scanning, and code quality assurance. That sentence names a field rather than a behaviour of this program: one data file enters, one schema file enters, and the behaviour is the judging of the one against the other.

![Minor separator: a short centred run of five bubbles in silt grey](sep-light.svg)

## Usage
`python3 main.py DATA_FILE SCHEMA_FILE [--data_type json|yaml] [--schema_type json|yaml] [--log_level LEVEL]`

![Major separator: a run of small separate bubbles in silt grey across the full width](sep-heavy.svg)

## Parameters
- `-h`: Show help message and exit
- `data_file`: Path to the API request/response data file (JSON or YAML). Required.
- `schema_file`: Path to the OpenAPI or schema definition file (JSON or YAML). Required.
- `--data_type`: Specify the data file type (json or yaml). Inferred from extension if omitted.
- `--schema_type`: Specify the schema file type (json or yaml). Inferred from extension if omitted.
- `--log_level`: Set the logging level. Choices: DEBUG, INFO, WARNING, ERROR, CRITICAL. Default: INFO.

> **Silt ledge: the README calls it OpenAPI here.** The parameter entry above styles schema_file as the path to the OpenAPI or schema definition file. That wording is preserved as printed and flagged here: the opening of this same file and the verified behaviour below state that an OpenAPI document is rejected, and a plain JSON Schema must be passed instead.

![Major separator: a run of small separate bubbles in silt grey across the full width](sep-heavy.svg)

## Verified behavior
- Valid data against a matching schema exits 0.
- Data that violates the schema exits 1 with the validation failure.
- A schema file containing an `openapi` or `swagger` key is rejected with exit 1 and the message that a plain JSON Schema must be passed instead.

![Minor separator: a short centred run of five bubbles in silt grey](sep-light.svg)

## License
See LICENSE.
