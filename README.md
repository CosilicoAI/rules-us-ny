# rules-us-ny

New York state rules encoded in Akoma Ntoso XML format.

## Directory Structure

```
rules-us-ny/
├── statutes/                    # New York Consolidated Laws
│   ├── tax-law/                 # NY Tax Law (Article 22, etc.)
│   └── social-services-law/     # NY Social Services Law
├── regulations/                 # NY Codes, Rules and Regulations (NYCRR)
│   └── nycrr/                   # Title 18, Title 20, etc.
└── README.md
```

## Data Sources

### Statutes
- **NY Consolidated Laws**: https://www.nysenate.gov/legislation/laws/CONSOLIDATED
- Primary sources: Tax Law, Social Services Law, General Business Law

### Regulations
- **NY Codes, Rules and Regulations (NYCRR)**: https://govt.westlaw.com/nycrr
- Key titles:
  - Title 18: Social Services
  - Title 20: Taxation and Finance

## Format

All documents are encoded in [Akoma Ntoso](http://www.akomantoso.org/) XML format, an OASIS standard for legislative documents.

## Related Repositories

| Repository | Description |
|------------|-------------|
| [arch](https://github.com/CosilicoAI/arch) | Policy document archive and source ingestion |
| [rac](https://github.com/CosilicoAI/rac) | Rules as Code DSL engine |
| [rac-us](https://github.com/CosilicoAI/rac-us) | US federal rules (Title 26 IRC, Title 7 SNAP) |

## License

Source statutes and regulations are public domain. Any original encoding work in this repository is licensed under Apache 2.0.
