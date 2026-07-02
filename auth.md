# auth.md

You are an agent. This is **jtjoo.com**, a static personal portfolio site. It serves public content and does **not** require authentication or registration to access.

Because there are no protected APIs, no OAuth flows, and no credential issuance, the registration endpoints listed in the authorization server metadata are **not implemented** — this document exists for discovery completeness so agents can confirm auth is unnecessary.

## Step 1 — Discover

The site publishes discovery metadata at standard well-known paths:

| Document | URL |
|---|---|
| Protected Resource Metadata | `/.well-known/oauth-protected-resource` |
| Authorization Server Metadata | `/.well-known/oauth-authorization-server` |

Both indicate the site has no authorization servers and no protected resources. All content is public.

## Step 2 — Access the site

No authentication is required. Fetch any public URL directly:

```
GET https://jtjoo.com/
```

No `Authorization` header needed. No access token needed.

## Step 3 — If you need to contact the site owner

For inquiries about agent or programmatic access:

- Email: clutch-silo-swan@duck.com
- LinkedIn: https://www.linkedin.com/in/jintaejoo

## Step 4 — If auth is added in the future

Check back at these same discovery endpoints. If `authorization_servers` is populated and `agent_auth` contains real endpoints, follow that configuration.
