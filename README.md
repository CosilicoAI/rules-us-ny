# rules-us-ny

New York state rules encoded in Akoma Ntoso XML format.

## Contents

| Law | Sections | Description |
|-----|----------|-------------|
| Tax Law | 1,411 | State income tax, sales tax, real property tax |
| Social Services Law | 726 | Public assistance, child welfare, Medicaid |
| Education Law | 1,946 | Schools, higher education, professional licensing |
| Public Health Law | 1,798 | Healthcare regulation, vital statistics, communicable diseases |
| Environmental Conservation Law | 1,849 | Environmental protection, natural resources |
| Labor Law | 774 | Employment standards, workplace safety, workers' comp |
| Penal Law | 892 | Criminal offenses, penalties, defenses |
| Criminal Procedure Law | 591 | Criminal justice procedures, rights of accused |
| Civil Practice Law | 814 | Civil litigation procedures, evidence rules |
| Domestic Relations Law | 175 | Marriage, divorce, family law |
| **Total** | **10,976** | |

## Directory Structure

```
rules-us-ny/
├── statutes/                           # New York Consolidated Laws
│   ├── tax-law/                        # NY Tax Law
│   ├── social-services-law/            # NY Social Services Law
│   ├── education-law/                  # NY Education Law
│   ├── public-health-law/              # NY Public Health Law
│   ├── environmental-conservation-law/ # NY Environmental Conservation Law
│   ├── labor-law/                      # NY Labor Law
│   ├── penal-law/                      # NY Penal Law
│   ├── criminal-procedure-law/         # NY Criminal Procedure Law
│   ├── civil-practice-law/             # NY Civil Practice Law and Rules
│   └── domestic-relations-law/         # NY Domestic Relations Law
├── regulations/                        # NY Codes, Rules and Regulations (NYCRR)
│   └── nycrr/                          # Title 18, Title 20, etc.
└── README.md
```

## Data Sources

### Statutes
- **NY Open Legislation API**: https://legislation.nysenate.gov/
- Converted from JSON API responses to Akoma Ntoso XML using [arch](https://github.com/CosilicoAI/arch)

### Regulations
- **NY Codes, Rules and Regulations (NYCRR)**: https://govt.westlaw.com/nycrr
- Key titles:
  - Title 18: Social Services
  - Title 20: Taxation and Finance

## Format

All documents are encoded in [Akoma Ntoso](http://www.akomantoso.org/) XML format, an OASIS standard for legislative documents.

### Sample File Structure

```xml
<?xml version="1.0" encoding="UTF-8"?>
<akomaNtoso xmlns="http://docs.oasis-open.org/legaldocml/ns/akn/3.0">
  <act name="TAX">
    <meta>
      <identification source="#ny-legislature">
        <FRBRWork>
          <FRBRthis value="/akn/us-ny/act/tax/section-1"/>
          <FRBRcountry value="us-ny"/>
          ...
        </FRBRWork>
      </identification>
    </meta>
    <body>
      <section eId="sec_1">
        <num>1</num>
        <heading>Short title</heading>
        <content>
          <p>This chapter shall be known as the "Tax Law."</p>
        </content>
      </section>
    </body>
  </act>
</akomaNtoso>
```

## Related Repositories

| Repository | Description |
|------------|-------------|
| [arch](https://github.com/CosilicoAI/arch) | Policy document archive and source ingestion |
| [rac](https://github.com/CosilicoAI/rac) | Rules as Code DSL engine |
| [rac-us](https://github.com/CosilicoAI/rac-us) | US federal rules (Title 26 IRC, Title 7 SNAP) |

## License

Source statutes and regulations are public domain. Any original encoding work in this repository is licensed under Apache 2.0.
