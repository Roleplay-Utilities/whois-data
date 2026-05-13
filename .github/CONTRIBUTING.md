# Contributing to whois-data

Thanks for your interest in helping improve `whois-data`! This repository is a public reference for registrar pricing for our WHOIS tool. We welcome any and all community contributions.

## What to contribute

`registrars.json` contains the data used by the project. You can help by:

- adding a new registrar or new TLDs for an existing registrar
- updating prices and renewal costs as defined by the registrar
- improving and updating registrar metadata such as name, links, pros, and cons
- removing outdated or incorrect entries when registrars are no longer relevant

## How to contribute

1. Fork the repository.
2. Create a new branch for your changes.
3. Edit `registrars.json` directly.
4. Commit your change with a descriptive message.
5. Open a pull request against the `main` branch.

## JSON format guidance

The file is a JSON array of registrar objects. Each registrar should include at least:

- `id`: a short, unique identifier (lowercase, no spaces)
- `name`: registrar display name
- `links`: object with relevant URLs such as `home` and `tlds`
- `pros`: array of short positive notes
- `cons`: array of short negative notes
- `tlds`: object mapping TLDs to pricing metadata

Example entry:

```json
{
  "id": "namecheap",
  "name": "Namecheap",
  "links": {
    "home": "https://www.namecheap.com/"
  },
  "pros": ["Cheap", "Good UI"],
  "cons": ["Heavy upsells"],
  "tlds": {
    "com": { "base": "~14.98", "renew": "~18.48", "last_checked": "5/13/2026" }
  }
}
```

## What to include for TLDs

For each TLD, please provide:

- `base`: registration price as stated on the registrar
- `renew`: renewal price as stated on the registrar
- `last_checked`: the date the price was last confirmed

If a field is not available, keep the structure consistent and omit only values you cannot verify. If you feel we need to add a new field please let us know!

## Review checklist

Before submitting a pull request, please verify:

- the JSON is valid
- `id` value is the same as the registrar name in lowercase
- URLs are correct and use HTTPS where possible
- prices and dates are formatted consistently and have been verified
- entries are factual and not promotional

## Need help?

If you are unsure about a registrar entry or TLD data, open an issue first and describe what you want to add or update. That helps maintainers review changes more quickly.

Thank you for contributing!
