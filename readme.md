# Sort Schema Args

Plugin to ensure sorting order of arguments in GraphQL. It should be used with [graphql-code-generator/](https://www.graphql-code-generator.com/).
While not required by the spec, some plugins expect the order to match, or they will fail.

It builds on top of the normal GraphQL introspection plugin, so you can use this instead.

## Setup

```yaml
schema: my-schema.graphql
documents: "./src/**/*.graphql"
generates:
  output.ts:
    - "@charlietango/sort-schema-args"
```

### Umbraco Heartcore fixes

The applies a set of fixes need to fix Umbraco Heartcore.

```yaml
schema: my-schema.graphql
documents: './src/**/*.graphql'
generates:
  output.ts:
    plugins:
      - '@charlietango/sort-schema-args'
          heartcore: true
```
