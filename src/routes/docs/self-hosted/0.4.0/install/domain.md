---
section: self-hosted/0.4.0/self-hosted
title: Domain
---

<script context="module">
  export const prerender = true;
</script>

# Domain

Gitpod requires a domain resolvable by some nameserver (typically a public domain name, e.g. `your-domain.com`).
As Gitpod launches services and workspaces on additional subdomains it also needs two wildcard domains.
For example:

    your-domain.com
    *.your-domain.com
    *.ws.your-domain.com

Installing Gitpod on a subdomain works as well. For example:

    gitpod.your-domain.com
    *.gitpod.your-domain.com
    *.ws.gitpod.your-domain.com
