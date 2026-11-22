# Flatverify OpenAPI

The OpenAPI 3.1 description of the [Flatverify](https://flatverify.com) REST API. Flatverify checks whether an email
address can receive mail, on a flat monthly price. Every plan is unlimited; plans differ only in speed.

- YAML: https://raw.githubusercontent.com/argorant/flatverify-openapi/main/flatverify-openapi.yaml
- JSON: https://raw.githubusercontent.com/argorant/flatverify-openapi/main/flatverify-openapi.json
- Docs: https://flatverify.com/docs
- Base URL: `https://app.flatverify.com/api/v1`, header `Authorization: Bearer fv_...`

| Method | Path | What it does |
| --- | --- | --- |
| POST | `/verify` | Verify one email and get the result right away |
| POST | `/verify/bulk` | Start a bulk job for up to 200,000 addresses |
| GET | `/jobs/{id}` | Job status and counts |
| GET | `/jobs/{id}/results` | Results as paged JSON (`format=json`) or CSV |
| GET | `/account` | Your plan and speed |

## Use cases

1. **Generate a client** in any language with OpenAPI Generator or your favourite tool, if there is no official SDK
   for it yet.
2. **Import into Postman, Insomnia, Bruno or Hoppscotch** to try every call with your key. The ready Postman
   collection is in the public Flatverify API workspace.
3. **Give an AI agent or a no-code platform the API** (GPT Actions, agent frameworks, custom connectors) by pointing
   it at the raw URL above.
4. **Mock the API in your tests** with Prism or a similar tool, so your signup or import flow can be tested offline.

Official SDKs: [JavaScript and TypeScript](https://github.com/argorant/flatverify-js) (`npm install flatverify`),
[Python](https://github.com/argorant/flatverify-python). MCP server: https://github.com/argorant/flatverify-mcp.

Flatverify by Argorant. This description is MIT licensed.
