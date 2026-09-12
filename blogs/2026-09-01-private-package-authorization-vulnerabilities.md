---
title: "Private package authorization vulnerabilities"
url: "/blog/private-package-authorization-vulnerabilities"
date: "2026-09-01"
feed_url: "https://hex.pm/feeds/blog.xml"
---
On 24 August 2026 we found and fixed two vulnerabilities in how hex.pm issues OAuth tokens. Both could give an account read access to private packages of an organization it was not entitled to. Neither was being exploited when we found them: no active token carried a scope for an organization its holder could not access.
