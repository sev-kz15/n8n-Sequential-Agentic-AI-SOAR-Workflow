# Sequential Agentic AI SOAR Platform — n8n workflow

Full-screen, read-only canvas of the n8n workflow behind a three-agent SOC automation pipeline
for SME environments. Companion to an research poster, the poster's QR code opens this page.

| File | Purpose |
|---|---|
| `index.html` | Lightweight canvas renderer of the workflow — pan, pinch-zoom, tap a node for its details |
| `n8n.html` | The same workflow in n8n's own preview component (`@n8n_io/n8n-demo-component`) |
| `workflow.json` | The exported workflow, sanitised for public release |

## Sanitisation

Environment-specific values — hosts, IP addresses, credential references, webhook paths, cloud
resource names and instance identifiers — are replaced with placeholders such as `<DC_IP>` and
`<OLLAMA_HOST>`. No secrets are present; n8n exports reference credentials by ID only, and those
IDs are redacted. This copy is for viewing and will not run as-is.


## Rendering note

`index.html` draws the workflow itself on a single `<canvas>` sized to the screen, so its memory
use is fixed at any zoom level. It was built after n8n's preview — the full n8n editor running
in an iframe — exhausted memory on iPhones during rapid zooming.

`n8n.html` still uses n8n's hosted preview service (`n8n-preview-service.internal.n8n.cloud`),
which receives the workflow JSON above.
