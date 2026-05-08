# Narrative Attack Resistance Layer

## Purpose
Large institutions under scrutiny predictably deploy specific counter-narratives. This layer pre-armors each evidence package against the six most common attack vectors.

## Attack Typology & Defense Matrix

| Attack Vector | Institution Claim | Pre-Defense Strategy |
|--------------|------------------|---------------------|
| **"Out of context"** | "You cherry-picked / took that out of context" | Preserve FULL communication threads — never excerpt without surrounding text. Annotate excerpts with links to full source. |
| **"Edited screenshot"** | "That screenshot is fabricated or edited" | Publish SHA-256 hash of original screenshot. Store original file in WORM. Submit RFC 3161 timestamp at capture. Never redact screenshots in image editor — use text overlay on copy. |
| **"Misinterpretation"** | "You misunderstood the technical/legal meaning" | Maintain contemporaneous legal annotations by qualified counsel. Record definitions of key terms at time of collection. Cite specific regulatory text. |
| **"Unauthorized publication"** | "That document was obtained illegally / published without authorization" | Document lawful acquisition basis at collection: FOIA request, public filing, authorized disclosure, etc. If leaked, track chain carefully and consult counsel before use. |
| **"Privacy violation"** | "You violated GDPR / data protection laws" | Maintain redaction log showing exactly what was redacted and why. Record lawful basis for processing (public interest, journalism exemption, regulatory purpose). Never publish unredacted PII. |
| **"Outdated / no longer relevant"** | "That was years ago, things have changed" | Timestamp every item. If presenting historical evidence, include contemporaneous context. Show pattern persistence if applicable. Track whether issue was remediated. |

## Evidence Integrity Checklist (Pre-Publication)
Before any external publication, verify:

- [ ] Full source available (not just excerpt)
- [ ] Original file hash computed and stored
- [ ] Timestamp proof exists
- [ ] Redaction log complete
- [ ] Lawful acquisition basis documented
- [ ] No PII exposed
- [ ] Context annotations written
- [ ] Counter-argument anticipated and addressed
- [ ] Confidence score assigned
- [ ] Tier classification verified

## If Attacked
1. **Do not delete or alter** any evidence in response to an attack
2. **Publish the pre-existing hash** to prove no alteration
3. **Release full context** if partial was shared
4. **State the confidence score** transparently
5. **Let the evidence speak** — avoid escalating rhetoric
6. **Document the attack** as a data point in the institutional pattern file

## Pattern Recognition for Institutions
Track each institution's attack playbook:
```
INSTITUTION ATTACK PATTERN LOG
───────────────────────────────
Institution:    {name}
Total Attacks:  {count}

Standard Playbook:
  1. {first move — e.g., deny receipt}
  2. {second move — e.g., claim misunderstanding}
  3. {third move — e.g., attack credibility}

Most Effective Defense:
  {what worked}
```
