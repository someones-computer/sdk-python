# someones.computer SDK — Python

A generated client for the [someones.computer](https://someones.computer) `/api` surface —
Organizations, Applications, Deployments, Managed Services, Swarms, and the rest of the
JSON-LD/Hydra API described at `/api/docs`.

Generated with [openapi-generator](https://openapi-generator.tech) (`python` generator) from
this API's OpenAPI 3 spec. It is **not hand-maintained** — see
[docs/sdk-generation.md](https://git.grey.ooo/Grey.ooo/Someones.Computer/src/branch/main/docs/sdk-generation.md)
in the main repo for the pipeline that produces it, and open issues there rather than editing
generated code here directly.

## Install

```bash
pip install someones-computer-sdk
```

## Authentication

Every operation takes a bearer token — the same `ApiToken` secret the platform's own `/cli`
API accepts (`Authorization: Bearer <token>`). Issue one from the control panel under
**Settings → API tokens**, then:

```python
import someones_computer_sdk

config = someones_computer_sdk.Configuration(access_token="<your token>")
with someones_computer_sdk.ApiClient(config) as client:
    organizations = someones_computer_sdk.OrganizationApi(client)
```

## Status

This is an early, mechanically generated SDK — method and type names follow the OpenAPI
spec's default `operationId` scheme rather than hand-picked names. Cleaning that up is
tracked upstream; expect method names to improve in a future release without a change in
what they do.

## License

MIT — see [LICENSE](LICENSE).
