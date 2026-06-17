# Workflows Automation with n8n

[![Validate workflows](https://github.com/fariasangelica/workflows-automation-with-n8n/actions/workflows/validate-workflows.yml/badge.svg)](https://github.com/fariasangelica/workflows-automation-with-n8n/actions/workflows/validate-workflows.yml)

n8n workflow exports stored as JSON in [`workflows/`](workflows/).

## Workflows

| Workflow | File | Description |
|----------|------|-------------|
| Currency Exchange | [`currency-exchange.json`](workflows/currency-exchange.json) | Form + exchange rate lookup |

### Currency Exchange

Form to pick base/target currencies and fetch the rate from [open.er-api.com](https://open.er-api.com/).

```
Form Trigger → HTTP Request → Edit Fields
```

![n8n workflow diagram for Currency Exchange](docs/images/currency-exchange-workflow.png)

![Currency Exchange web form](docs/images/currency-exchange-form.png)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
