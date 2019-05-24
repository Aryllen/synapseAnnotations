# Schemas

Example schemas for AMP-AD and NF. They reference the definitions in the
`definitions/` folder. To check that the schemas are valid JSON Schema using
[ajv-cli](https://github.com/jessedc/ajv-cli):

```
ajv compile -s ampad_schema.json -r "definitions/*.json"
ajv compile -s nf_schema.json -r "definitions/*.json"
```

To validate sample data against the AMP-AD schema:

```
ajv -s ampad_schema.json -r "definitions/*.json" -d ampad_demo.json
```
