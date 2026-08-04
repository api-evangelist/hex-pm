---
title: "Deprecating Basic Authentication on the API"
url: "/blog/deprecating-basic-auth"
date: "2026-07-28"
feed_url: "https://hex.pm/feeds/blog.xml"
---
Hex.pm will disable HTTP Basic authentication on the API. Basic auth sends a username and password on every request and has no way to carry a second factor, which blocks us from requiring two-factor authentication for API access. To move forward on that goal, we are phasing Basic auth out of the API entirely.
