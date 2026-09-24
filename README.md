# Sequential Agentic AI SOAR Platform — n8n workflow

Full-screen, read-only canvas of the n8n workflow behind a three-agent SOC automation pipeline
for SME cloud environments. Companion to an Honours research poster (STEM7700, Flinders
University); the poster's QR code opens this page.

| File | Purpose |
|---|---|
| `index.html` | Renders the workflow with n8n's open-source preview component (`@n8n_io/n8n-demo-component`) |
| `workflow.json` | The exported workflow, sanitised for public release |

## Sanitisation

Environment-specific values — hosts, IP addresses, credential references, webhook paths, cloud
resource names and instance identifiers — are replaced with placeholders such as `<DC_IP>` and
`<OLLAMA_HOST>`. No secrets are present; n8n exports reference credentials by ID only, and those
IDs are redacted. This copy is for viewing and will not run as-is.

## Layout adjustments

n8n's preview renderer draws sticky-note text about 1.28× larger than a typical self-hosted
editor, which pushed each layer's description out of its box. The layer notes' blank-line
spacing, heights and top edges are adjusted so every heading and description renders inside its
box and clear of the nodes. No node, connection or wording is changed.

## Rendering note

The canvas is drawn by n8n's hosted preview service (`n8n-preview-service.internal.n8n.cloud`),
which receives the workflow JSON above. The page depends on that service being available.
