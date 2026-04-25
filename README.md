# Motorical SMTP Examples

Practical examples for sending, receiving, and verifying production email with Motorical SMTP.

Motorical SMTP is email infrastructure for applications that need HTTP email sending, SMTP credentials, isolated Motorical SMTP Motor Blocks, delivery logs, signed webhooks, and rate-aware sending.

## Examples

| Example | Use it when you need |
| --- | --- |
| [`node-http-send`](./node-http-send) | Send transactional email through the Motorical SMTP HTTP Send API, starting with `dryRun: true`. |
| [`node-webhooks`](./node-webhooks) | Receive delivery events and verify `X-Motorical-Signature`. |
| [`smtp-nodemailer`](./smtp-nodemailer) | Send email from an existing Node.js app that already uses SMTP. |
| [`python-http-send`](./python-http-send) | Send transactional email from Python over HTTPS. |
| [`nextjs-contact-form`](./nextjs-contact-form) | Build a backend-only contact form route with a Motorical SMTP API key. |

## Key Concepts

Use a Motorical SMTP Motor Block as the boundary for an application, environment, domain, tenant, or sending risk profile. Each SMTP Motor Block can have its own domain, API keys, SMTP credentials, rate policy, delivery logs, and webhook endpoints.

## Credentials

Copy the `.env.example` file inside each example and fill in values from your Motorical SMTP dashboard. Keep all keys server-side.

Common variables:

```bash
MOTORICAL_SMTP_API_KEY=mk_live_YOUR_MOTOR_BLOCK_API_KEY
MOTORICAL_SMTP_FROM=sender@yourdomain.com
MOTORICAL_SMTP_TO=recipient@example.com
```

Never commit real API keys, webhook secrets, SMTP passwords, tenant IDs, or private URLs.

## Documentation

- Motorical SMTP docs: https://docs.motorical.com
- HTTP Send API quickstart: https://docs.motorical.com/send-email/http-api-quickstart
- SMTP integration: https://docs.motorical.com/smtp-integration/code-examples
- Webhooks: https://docs.motorical.com/guides/webhook-delivery-events
- AI agent quickstart: https://docs.motorical.com/ai
- Swagger UI: https://api.motorical.com/api/public/docs
- OpenAPI JSON: https://api.motorical.com/api/public/openapi.json

## Run Checks

From the repository root:

```bash
npm run check
```

The root check validates JavaScript syntax and Python syntax without requiring real credentials.

## License

MIT
