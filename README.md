# Sequential Agentic AI SOAR Platform — n8n workflow

Interactive, read-only view of the n8n workflow behind a three-agent SOC automation pipeline
for SME cloud environments. Companion to an Honours research poster (STEM7700, Flinders
University).

**View it:** open `index.html` via GitHub Pages.

## What's here

| File | Purpose |
|---|---|
| `index.html` | Renders the workflow with n8n's open-source preview component (`@n8n_io/n8n-demo-component`) |
| `workflow.json` | The exported workflow, sanitised for public release |

## Sanitisation

Environment-specific values — hosts, IP addresses, credential references, webhook paths, cloud
resource names and instance identifiers — are replaced with placeholders such as `<DC_IP>` and
`<OLLAMA_HOST>`. No secrets are present; n8n exports reference credentials by ID only, and those
IDs are redacted. This copy is for viewing and will not run as-is.

## Rendering note

The canvas is drawn by n8n's hosted preview service (`n8n-preview-service.internal.n8n.cloud`),
which receives the workflow JSON above. The page depends on that service being available.
