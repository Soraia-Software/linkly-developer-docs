# Linkly API Reference

Public API documentation for [developer.linkly.events](https://developer.linkly.events), built with [Scalar](https://scalar.com).

## Structure

```
index.html      # Scalar embed — UI config (logo, theme, auth placeholder)
openapi.yaml    # OpenAPI 3.0 spec — endpoints, schemas, examples
public/
  linkly-icon.png
  linkly-logo-white.png
```

## Updating the docs

All content lives in `openapi.yaml`. Edit it directly — no build step needed.

Common changes:
- **Add/change a field**: find the relevant schema under `components/schemas` and add or edit the property
- **Add an endpoint**: add a new path under `paths`, following the existing pattern
- **Fix an example**: find the `example:` value under the relevant response

Push to `main` and Cloudflare Pages deploys automatically within ~30 seconds.

## Local preview

```bash
npx serve . -p 4000
```

Then open [http://localhost:4000](http://localhost:4000).

## Deployment

Hosted on Cloudflare Pages. Connected to this repo's `main` branch — every push deploys to [developer.linkly.events](https://developer.linkly.events) automatically.
