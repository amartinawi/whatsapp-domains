# whatsapp-domains

A plain-text list of domains and hostnames used by or known for WhatsApp services:
messaging, WhatsApp Web, media CDN, calls, Business API, `wa.me` / `wl.co` links and brand sites.

## Files

| File | Contents |
|------|----------|
| [`whatsapp-domains.txt`](whatsapp-domains.txt) | Full list, one domain per line, grouped into commented sections |
| [`whatsapp-wildcards.txt`](whatsapp-wildcards.txt) | Short suffix/wildcard ruleset (`*.whatsapp.net`, `*.cdn.whatsapp.net`, ...) |

Raw URLs:

```
https://raw.githubusercontent.com/amartinawi/whatsapp-domains/main/whatsapp-domains.txt
https://raw.githubusercontent.com/amartinawi/whatsapp-domains/main/whatsapp-wildcards.txt
```

## Sections in `whatsapp-domains.txt`

1. **WhatsApp root domains**: `whatsapp.com`, `whatsapp.net`, `wa.me`, `wl.co`, ... Match these as suffixes.
2. **Meta shared infrastructure**: `facebook.com`, `fbcdn.net`, `fbsbx.com`, `instagram.com`, ... WhatsApp media, calls and API integrations rely on these, but blocking or routing them also affects Facebook and Instagram.
3. **Associated / defensive registrations**: `wa.com`, `whatsapp-plus.*`. Linked to WhatsApp but not required service endpoints.
4. **WhatsApp hosts**: exact hostnames (core `e1`–`e16.whatsapp.net` chat endpoints, `*-fallback` hosts, regional media nodes under `cdn.` / `fna.` / `snr.whatsapp.net`, ...).
5. **WhatsApp hosts on Meta infrastructure**: `whatsapp-cdn-shv-*.fbcdn.net`, `whatsapp-chatd-edge-*.facebook.com`, `graph.facebook.com`, ...

## Notes

- Regional media nodes change constantly, so the exact-host list will never be complete. Prefer the suffix rules in `whatsapp-wildcards.txt` where your tool supports them.
- Being listed or resolving in DNS does not prove a hostname is still a live client-facing endpoint.
- WhatsApp also connects to Meta-owned IP ranges directly, so a domain list alone won't fully block or route it. See [HybridNetworks/whatsapp-cidr](https://github.com/HybridNetworks/whatsapp-cidr) for CIDR lists.

## Sources

Merged and deduplicated from:

- [blocklistproject/Lists](https://github.com/blocklistproject/Lists)
- [jmdugan/blocklists](https://github.com/jmdugan/blocklists)
- [sefinek/Sefinek-Blocklist-Collection](https://github.com/sefinek/Sefinek-Blocklist-Collection)
- [v2fly/domain-list-community](https://github.com/v2fly/domain-list-community)
- [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)
- [HybridNetworks/whatsapp-cidr](https://github.com/HybridNetworks/whatsapp-cidr)
- [ooni/spec ts-018 WhatsApp test](https://github.com/ooni/spec/blob/master/nettests/ts-018-whatsapp.md)

Pull requests with new domains are welcome.
