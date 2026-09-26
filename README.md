# whatsapp-domains

A plain-text list of domains and hostnames used by or known for WhatsApp services:
messaging, WhatsApp Web, media CDN, calls, Business API, `wa.me` links and brand sites.

**File:** [`whatsapp-domains.txt`](whatsapp-domains.txt), one domain per line. Lines starting with `#` are comments.

Raw URL:

```
https://raw.githubusercontent.com/amartinawi/whatsapp-domains/main/whatsapp-domains.txt
```

## Notes

- Root domains (`whatsapp.com`, `whatsapp.net`, `wa.me`, ...) are listed first. Matching on them as suffixes covers most traffic; the explicit hostnames are there for tools that need exact matches.
- WhatsApp media, calls and API integrations also rely on Meta infrastructure (`facebook.com`, `fb.com`, `facebook.net`, `fbcdn.net`, `fbcdn.com`, `fbsbx.com`, `instagram.com`, `cdninstagram.com`). Root domains are meant as suffixes (`*.fbcdn.net` etc.). Blocking or routing them also affects Facebook/Instagram.
- WhatsApp also connects to Meta-owned IP ranges directly, so a domain list alone won't fully block or route it.

## Sources

Merged and deduplicated from:

- [blocklistproject/Lists](https://github.com/blocklistproject/Lists)
- [jmdugan/blocklists](https://github.com/jmdugan/blocklists)
- [sefinek/Sefinek-Blocklist-Collection](https://github.com/sefinek/Sefinek-Blocklist-Collection)
- [v2fly/domain-list-community](https://github.com/v2fly/domain-list-community)
- [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)

Pull requests with new domains are welcome.
