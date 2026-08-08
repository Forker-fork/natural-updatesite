# Natural — Eclipse update site

Prebuilt [p2](https://wiki.eclipse.org/Equinox/p2) update site for the **Natural** plugin:
Cucumber and JBehave editors for Eclipse.

This repository contains **only the built artifacts**. It is generated output, not source.

## Install

Update site URL:

```
https://forker-fork.github.io/natural-updatesite/
```

1. **Help → Install New Software…**
2. **Add…** → paste the URL above → name it `Natural` → **Add**
3. Tick **Cucumber** and **Jbehave**
4. **Next → Finish**, then restart Eclipse

## Requirements

| | |
|---|---|
| Eclipse | 2025-12 or later (tested on 2026-06 / 4.40) |
| Java | 25 |
| Xtext | 2.43 (from the Eclipse release train) |

> **2.0.0 is a breaking release.** Java 8 support is dropped and the minimum Eclipse
> version is 2025-12, because Xtext 2.43 requires it.

## Contents

| Bundle | Version |
|---|---|
| `org.agileware.natural.common` | 2.0.0 |
| `org.agileware.natural.cucumber` | 2.0.0 |
| `org.agileware.natural.cucumber.ide` | 2.0.0 |
| `org.agileware.natural.cucumber.ui` | 2.0.0 |
| `org.agileware.natural.jbehave` | 2.0.0 |
| `org.agileware.natural.jbehave.ide` | 2.0.0 |
| `org.agileware.natural.jbehave.ui` | 2.0.0 |

Features: `org.agileware.natural.cucumber.feature`, `org.agileware.natural.jbehave.feature`
(source features included).

## Known limitations

- Cucumber Expressions (`{int}`, `{string}`) are not supported — step definition
  annotations must be regular expressions, e.g. `@Given("^I have (\\d+) cukes$")`
- Only the `io.cucumber.java.en` annotation package is recognised
- `.story` (JBehave) files have no Ctrl+click navigation to step definitions
- English Gherkin keywords only; the `*` step keyword is not supported

## License

[Eclipse Public License 1.0](LICENSE). Originally created by Roberto Lo Giacco —
see the [upstream project](https://github.com/rlogiacco/Natural).

## Attribution

This is a **fork** of [rlogiacco/Natural](https://github.com/rlogiacco/Natural),
originally created by Roberto Lo Giacco.

- **Original work** — © Roberto Lo Giacco &lt;rlogiacco@gmail.com&gt; and others, 2012
- **Modifications in this fork** — © 2026 Hariharan M

Both are licensed under the [Eclipse Public License 1.0](LICENSE). Copyright in the
original work remains with its respective authors; nothing here alters or supersedes the
EPL 1.0. See [NOTICE](NOTICE) for the detailed attribution and a summary of the changes
made in this fork.
