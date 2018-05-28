# terraform-provider-snowflake

terraform-provider-snowflake is a [Terraform](https://www.terraform.io/) provider for the [Snowflake](https://www.snowflake.net/) cloud data warehouse.

## Supported types

### Resources

- snowflake_database
- snowflake_schema

### Data Sources

- snowflake_schema

## Configuring the provider

Right now the provider is configured by providing the full DSN which is fed through to the gosnowflake connector. Here are some examples of the format of the DSN:

```text
user[:password]@account/database/schema[?param1=value1&paramN=valueN]
user[:password]@account/database[?param1=value1&paramN=valueN]
user[:password]@host:port/database/schema?account=user_account[?param1=value1&paramN=valueN]
```

If a variable is set up for the DSN it can be configured as an environment variable or in `terraform.tfvars`.