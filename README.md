# Workflows Automation with n8n

n8n workflow exports stored as JSON in `workflows/`.

## Currency Exchange

[`workflows/currency-exchange.json`](workflows/currency-exchange.json) — form to pick base/target currencies and fetch the exchange rate from [open.er-api.com](https://open.er-api.com/).

```
Form Trigger → HTTP Request → Edit Fields
```

![Workflow](docs/images/currency-exchange-workflow.png)

![Form](docs/images/currency-exchange-form.png)
