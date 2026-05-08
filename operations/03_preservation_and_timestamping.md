# Evidence Preservation — WORM Storage, RFC 3161 Timestamping & Legal Hold

## WORM Storage Requirements

### Primary (Cloud Immutable)
| Provider | Service | Configuration |
|----------|---------|---------------|
| AWS | S3 Object Lock | Governance mode, retention period 7 years |
| Azure | Immutable Blob Storage | Time-based retention, legal hold enabled |
| Wasabi | Immutable Buckets | Compliance mode, minimum 1 year retention |
| Backblaze | B2 Object Lock | Read-only, versioning enabled |

### Secondary (Local/Offline)
- Encrypted external drives stored in 2 geographic locations
- BitLocker/LUKS full-disk encryption
- Air-gapped when not in use
- Inventory manifest signed and timestamped

## RFC 3161 Trusted Timestamping

### Workflow
```
1. Generate SHA-256 hash of evidence file
2. Submit hash to Time Stamp Authority (TSA)
3. Receive signed timestamp token (.tsr file)
4. Verify token against TSA certificate chain
5. Store token alongside evidence
6. Record token reference in evidence manifest
```

### Recommended TSAs
| Provider | URL | Compliance |
|----------|-----|------------|
| DigiCert | timestamp.digicert.com | ETSI EN 319 422 |
| Sectigo | timestamp.sectigo.com | RFC 3161 |
| GlobalSign | timestamp.globalsign.com | ETSI compliant |
| FreeTSA | freetsa.org | Community (for development) |

### Verification Command (OpenSSL)
```bash
# Timestamp a file
openssl ts -query -data evidence.pdf -sha256 -out evidence.tsq
curl -H "Content-Type: application/timestamp-query"   --data-binary @evidence.tsq   https://timestamp.digicert.com -o evidence.tsr
openssl ts -verify -data evidence.pdf -in evidence.tsr   -CAfile cacert.pem

# Verify later
openssl ts -verify -data evidence.pdf -in evidence.tsr   -CAfile cacert.pem
```

## Legal Hold Procedures

### Trigger Events
Legal hold ACTIVATES when ANY of:
- Formal regulatory inquiry received (SEC/FSMA/FMA/ESMA)
- Civil litigation threatened or filed
- Whistleblower submission made to regulator
- Media investigation published naming targets
- Internal escalation threshold (see escalation doc) reached Level 3+

### Hold Actions
| Action | Implementation |
|--------|---------------|
| Freeze deletion | All evidence stores set to immutable |
| Disable purges | Retention policies overridden |
| Intensify logging | Access audit set to maximum detail |
| Notify team | All collectors informed of hold status |
| Stop routine culling | No evidence review/deletion cycles |
| Mirror repositories | Full copy to independent storage |

### Hold Release
Legal hold RELEASES only when:
- Written confirmation from legal counsel
- Statute of limitations has expired
- Regulatory matter formally closed
- Written notice preserved in evidence log

### Hold Log Template
```
LEGAL HOLD NOTICE
─────────────────
Hold ID:         LH-{YYYYMMDD}-{SEQ}
Issued by:       {name/role}
Date Issued:     {YYYY-MM-DD HH:MM UTC}
Trigger Event:   {description}
Scope:           {which evidence collections are covered}

Actions Taken:
  [ ] Immutable storage enabled
  [ ] Deletion disabled
  [ ] Audit logging intensified
  [ ] Team notified ({N} members)
  [ ] Backup created at {location}

Hold Released:   {date or PENDING}
Release Reason:  {if released}
```
