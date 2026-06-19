# Workflows Automation with n8n

[![Validate workflows](https://github.com/fariasangelica/workflows-automation-with-n8n/actions/workflows/validate-workflows.yml/badge.svg)](https://github.com/fariasangelica/workflows-automation-with-n8n/actions/workflows/validate-workflows.yml)

n8n workflow exports stored as JSON in [`workflows/`](workflows/).

## Workflows

| Workflow | File | Description |
|----------|------|-------------|
| Currency Exchange | [`currency-exchange.json`](workflows/currency-exchange.json) | Form + exchange rate lookup |
| Event Signup | [`event-signup.json`](workflows/event-signup.json) | Self-service event registration form |
| Contact Record | [`contact-record.json`](workflows/contact-record.json) | Structured partner contact record |
| Unnecessary Fields | [`unnecessary-fields.json`](workflows/unnecessary-fields.json) | Filter contact fields for mailing list |
| Timestamp | [`timestamp.json`](workflows/timestamp.json) | Event signup with submission timestamp |

### Currency Exchange

Form to pick base/target currencies and fetch the rate from [open.er-api.com](https://open.er-api.com/).

```
Form Trigger → HTTP Request → Edit Fields
```

**Output:** `Base Currency`, `Target Currency`, `Exchange Rate`

### Event Signup

Self-service form for Acme event attendees — collects first name, last name, and email, then outputs a clean registration record.

```
Form Trigger → Edit Fields
```

**Output:** `full_name`, `email`, `registered_at`

### Contact Record

A equipe de parcerias da Acme precisa de uma forma simples de registrar novos contatos de parceiros. Antes de conectar a um CRM real, eles querem um workflow que crie um registro de contato estruturado para inspecionar.

```
Manual Trigger → Edit Fields
```

**Output:** `company_name`, `contact`, `email`

### Unnecessary Fields

A equipe de parcerias da Acme cria registros de contato completos, mas o sistema de mailing list só precisa de nome e email — não da empresa. Você precisa adicionar uma etapa que filtre os campos desnecessários antes de passar os dados adiante.

```
Manual Trigger → Edit Fields → Edit Fields1
```

**Output:** `contact`, `email`

### Timestamp

A equipe de eventos da Acme quer saber exatamente quando cada participante se inscreveu, para acompanhar a velocidade das inscrições e encerrar o cadastro no momento certo. O formulário captura os dados do participante, mas você também precisa registrar o momento do envio.

```
Form Trigger → Edit Fields
```

**Output:** `Event name`, `Atendee name`, `Email`, `submitted_at`

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
