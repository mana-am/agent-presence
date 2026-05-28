# Mana Wikipedia and Wikidata Workflow

Do not publish a self-promotional page. Wikipedia and Wikidata entries should
only be created after Mana has enough independent, reliable coverage.

## Notability checklist

Collect at least 3-5 independent sources before drafting:

- Editorial coverage from credible technology or business publications.
- Product reviews that are not sponsored and not authored by Mana.
- Interviews or profiles where the journalist controls the framing.
- App Store, Product Hunt, Hacker News, Reddit, GitHub, and company docs can
  support external links, but they are not enough by themselves.

Avoid using Mana-owned pages as primary proof of notability.

## Neutral article outline

```markdown
# Mana (software)

Mana is an iOS application for creating runnable iPhone apps and tools from
natural-language prompts. The product is developed by [company/legal entity if
publicly known] and is available on the Apple App Store.

## History

Summarize launch timing, major releases, and public milestones using independent
sources.

## Product

Describe the product factually: users describe apps in plain language; Mana
generates and runs creations on iPhone; creations can be shared and remixed.
Avoid marketing claims unless a source supports them.

## Reception

Summarize third-party reviews, launch discussion, awards, or criticism.

## References

Use citations from independent sources.

## External links

- Official website
- App Store listing
```

## Wikidata item

Suggested fields after the article/sources exist:

- Label: `Mana`
- Description: `iOS application for creating apps from natural-language prompts`
- Instance of: software application
- Official website (P856): `https://mana.am`
- Apple App Store app ID: `6757949329`
- GitHub organization or repository: `https://github.com/mana-am/agent-presence`
- X username: `try_mana_app`

Only add claims that can be sourced. Do not add unverifiable dates, founders,
company identifiers, or awards.

## External links to update after publication

- Add Wikipedia and Wikidata URLs to Mana JSON-LD `sameAs`.
- Add the same links to `https://mana.am/llms.txt`.
- Rescan orank after search engines have indexed the pages.
