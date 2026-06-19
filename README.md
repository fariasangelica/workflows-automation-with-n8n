# Workflows Automation with n8n

[![Validate workflows](https://github.com/fariasangelica/workflows-automation-with-n8n/actions/workflows/validate-workflows.yml/badge.svg)](https://github.com/fariasangelica/workflows-automation-with-n8n/actions/workflows/validate-workflows.yml)

n8n workflow exports stored as JSON in [`workflows/`](workflows/).

## Workflows

| Workflow | File | Description |
|----------|------|-------------|
| Currency Exchange | [`currency-exchange.json`](workflows/currency-exchange.json) | Form + exchange rate lookup |
| Event Signup | [`event-signup.json`](workflows/event-signup.json) | Self-service event registration form |
| Contact Record | [`contact-record.json`](workflows/contact-record.json) | Structured partner contact record |

### Currency Exchange

Form to pick base/target currencies and fetch the rate from [open.er-api.com](https://open.er-api.com/).

```
Form Trigger → HTTP Request → Edit Fields
```

![n8n workflow diagram for Currency Exchange](docs/images/currency-exchange-workflow.png)

![Currency Exchange web form](docs/images/currency-exchange-form.png)

### Event Signup

Self-service form for Acme event attendees — collects first name, last name, and email, then outputs a clean registration record.

```
Event Signup (Form Trigger) → Edit Fields
```

**Output:** `full_name`, `email`, `registered_at`

![Event Signup workflow execution in n8n](docs/images/event-signup-workflow.png)

### Contact Record

A equipe de parcerias da Acme precisa de uma forma simples de registrar novos contatos de parceiros. Antes de conectar a um CRM real, eles querem um workflow que crie um registro de contato estruturado para inspecionar.

```
Manual Trigger → Edit Fields
```

**Output:** `company_name`, `contact`, `email`

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
