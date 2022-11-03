# Liquibase Deactivate Changelog Action
Official GitHub Action to run Liquibase Deactivate Changelog in your GitHub Action Workflow. For more information on how deactivate changelog works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Deactivate Changelog
Removes the changelogID from your changelog so it stops sending reports to Liquibase Hub
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/deactivate-changelog@v4.17.0
  with:
    # The root changelog
    # string
    # Required
    changelogFile: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase deactivate changelog action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/deactivate-changelog@v4.17.0
    with:
      changelogFile: ""
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
