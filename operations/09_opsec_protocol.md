# Operational Security (OPSEC) Protocol

## Threat Model
If the campaign becomes sensitive, adversaries may include:
- Institutional legal departments conducting discovery
- PR firms running opposition research
- Private investigators hired by targets
- State-level actors in certain jurisdictions
- Hacktivists or retaliatory actors

## Compartmentalization

### Identity Separation
| Identity | Purpose | Channels | Exposure |
|----------|---------|----------|----------|
| **Primary investigative identity** | All campaign work | Signal, Proton, encrypted | Known to trusted sources only |
| **Public-facing identity** | Media spokesperson | Standard email, phone | Public |
| **Technical identity** | Domain registrations, OSINT accounts | VPN, aliases | Masked |
| **Research identity** | Kaggle, data platform access | Separate account | Minimal |

### Information Compartments
```
Campaign Director ─── knows all
    ├── Evidence Team ─── knows evidence handling only
    ├── Legal Team ─── knows legal strategy only
    ├── Media Team ─── knows approved narratives only
    └── Research Team ─── knows data sources only
```

## Communications Security

### Required Tools
| Purpose | Tool | Configuration |
|---------|------|---------------|
| Messaging | Signal | Disappearing messages enabled, screenshot blocking |
| Email | ProtonMail | Encrypted, zero-access, aliases |
| File sharing | Proton Drive / Tresorit | End-to-end encrypted |
| Voice/video | Signal | Always verify safety numbers |
| Password mgmt | Bitwarden / 1Password | Strong master password, 2FA |

### Prohibited Tools
- WhatsApp (Meta-owned, weak encryption metadata)
- Telegram (default not E2EE, server-side storage)
- Google Docs/Drive (no E2EE, US jurisdiction)
- Slack/Discord (no E2EE, corporate accessible)
- SMS (zero encryption)

## Endpoint Security

| Measure | Implementation |
|---------|---------------|
| Full disk encryption | LUKS (Linux), BitLocker (Windows), FileVault (macOS) |
| VPN | Mullvad or ProtonVPN — kill switch enabled |
| Antivirus | Minimal — use app whitelisting instead |
| Browser | Firefox + uBlock Origin + container tabs |
| Search | Startpage or DuckDuckGo for investigation |
| Hardware | Separate device for sensitive work if possible |

## Operational Rules

1. **Never discuss campaign details on unencrypted channels** — not even "how's the project going"
2. **No campaign cloud services on personal devices** — compartmentalize
3. **Assume metadata is visible** — Signal hides content, not who talks to whom
4. **Meeting security** — no phones in sensitive meetings, assume room may be monitored
5. **Travel security** — use burner devices for high-risk travel, no sensitive data crosses borders
6. **Social media hygiene** — no cross-posting between identities, no location sharing
7. **Source protection** — never share source identity beyond need-to-know
8. **Cleaner discipline** — regularly purge unnecessary data from active devices

## Incident Response

If compromise is suspected:
1. Immediately rotate all credentials
2. Assume all communications on compromised channel are captured
3. Activate legal hold if evidence may be affected
4. Conduct damage assessment
5. Notify trusted sources whose relationship may be exposed
6. Engage external security counsel if warranted
