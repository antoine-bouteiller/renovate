# renovate

Shared [Renovate](https://docs.renovatebot.com/) presets for my repositories.

```json5
{
  $schema: 'https://docs.renovatebot.com/renovate-schema.json',
  extends: ['github>antoine-bouteiller/renovate'],
}
```

| Preset                                              | Content                                                          |
| --------------------------------------------------- | ---------------------------------------------------------------- |
| `github>antoine-bouteiller/renovate`                | Base settings, vulnerability alerts, and the three presets below |
| `github>antoine-bouteiller/renovate:automerge`        | Auto-merge patch and minor updates, and GitHub Actions digests    |
| `github>antoine-bouteiller/renovate:groups`           | Package groups; a group without matching packages is a no-op     |
| `github>antoine-bouteiller/renovate:semantic-commits` | Conventional commit types, scopes, and update-type labels        |

Keep repository-specific rules (custom managers, disabled packages, strategy overrides) in the repository's own `renovate.json5`; its `packageRules` apply after these presets.
