# Hex.pm

Package registry for the Erlang and Elixir ecosystems with a REST API for searching packages, accessing metadata, managing releases, and user authentication.

## Overview

Hex.pm is the central package registry for the BEAM ecosystem, serving Erlang, Elixir, and Gleam developers. It provides a REST API for package discovery, metadata retrieval, release management, authentication, API key management, and organization administration.

**Base URL:** `https://hex.pm/api`  
**Repository Endpoint:** `https://repo.hex.pm`  
**Documentation:** https://hex.pm/docs  
**API Specification:** https://github.com/hexpm/specifications

## Key API Capabilities

- Search and retrieve package metadata (25,500+ packages)
- Publish, retire, and manage package releases
- Manage API keys and OAuth2 device authorization
- Administer organizations and package ownership
- Access private repositories (paid plans)
- Retrieve package documentation

## Authentication

| Method | Header | Notes |
|--------|--------|-------|
| API Token | `Authorization: {token}` | Created via web UI or `/keys` endpoint |
| OAuth2 Bearer | `Authorization: Bearer {token}` | Device authorization grant (RFC 8628) |
| Basic Auth | `-u "username"` | Deprecated; token generation endpoints only |

Write operations may require 2FA via the `x-hex-otp` header.

## Rate Limits

| Type | Limit |
|------|-------|
| Unauthenticated | 100 requests/minute per IP |
| Authenticated | 500 requests/minute per token |

Rate limit headers: `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`

## Pricing

| Plan | Price | Notes |
|------|-------|-------|
| Open Source | Free | Unlimited public packages |
| Private Packages | $7/month or $70/year | Unlimited private packages, 30-day trial |
| Enterprise | Custom | Self-hosted, mirroring, whitelisting |

## Resources

- [API Specification (API Blueprint)](https://github.com/hexpm/specifications/blob/master/apiary.apib)
- [Protocol Specifications](https://github.com/hexpm/specifications)
- [Source Code](https://github.com/hexpm/hexpm)
- [Status Page](https://status.hex.pm)
- [Security Advisories](https://osv.dev/list?ecosystem=Hex)
- [Blog](https://hex.pm/blog)

## Support

- General support: support@hex.pm
- Security issues: security@hex.pm
- GitHub issues: https://github.com/hexpm/hexpm/issues
