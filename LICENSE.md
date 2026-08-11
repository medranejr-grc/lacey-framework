# License

This repository is licensed in two parts, because it contains two different kinds of thing.

| Path | License | Why |
|---|---|---|
| `docs/`, `README.md`, `SCOPE.md`, `PRINCIPLES.md`, `CODE_OF_CONDUCT.md`, `LICENSE.md` | **CC BY-SA 4.0** | Essays, argument, licensing explanation, and adapted community policy. Share and adapt freely with credit; derivatives stay open under the same terms. |
| `templates/`, `examples/`, `.github/`, `.gitattributes`, `CONTRIBUTING.md` | **CC0 1.0** (public domain dedication) | Reusable operational material. No attribution required, no conditions inherited. |

## Why the split

The templates and examples exist to be copied into someone's agent configuration and modified beyond
recognition. A share-alike term on that material would be a trap rather than a protection: it would
mean that adapting the skeleton into a company's system prompt could place licensing conditions on
the system it governs. No enterprise legal review would clear that, and the framework would fail to
reach exactly the deployments it was written for.

Attribution requirements were also dropped for that half, deliberately. Requiring credit *inside a
system prompt* is awkward at best and unenforceable in practice. Credit lives with the essays, where
it belongs and where it works.

The essays are a different case. They are an argument, and an argument benefits from staying open:
if someone builds on the reasoning here, that extension should be as available as the original was.

**Practical summary:** quote the essays with credit and keep derivatives open. Take the templates and
do whatever you want, including in closed commercial products, with no obligation to anyone.

## Tell us if it reaches production

Neither license requires anyone to notify the author, and commercial use of the CC0 materials is
welcome. Still, one of the greatest rewards for the author would be learning that the Lacey
Framework's constitutional layer had reached a real commercial production environment.

If you are willing and authorized to share, please submit a voluntary
[`field result`](.github/ISSUE_TEMPLATE/field-result.yml). Describe what was used, where it entered
the system, and what you observed. A public summary, an anonymized report, or simply notice that it
is running would all be meaningful. Do not disclose protected architecture, private prompts,
credentials, employer or client information, or anything you do not have the right to publish.

This invitation is not a license condition, attribution requirement, certification, or request for
confidential information.

## Full license text

- **CC BY-SA 4.0:** <https://creativecommons.org/licenses/by-sa/4.0/legalcode>
  Summary: <https://creativecommons.org/licenses/by-sa/4.0/>
- **CC0 1.0:** <https://creativecommons.org/publicdomain/zero/1.0/legalcode>
  Summary: <https://creativecommons.org/publicdomain/zero/1.0/>

Per-directory `LICENSE` files restate which applies where.

## Attribution

When crediting the CC BY-SA material:

> The Lacey Framework, by Michael E. Drane Jr. Licensed under CC BY-SA 4.0.

## Third-party material

External research, vendor documentation, and standards remain under their own terms. Limited
quotations are attributed inline and used for criticism or explanation. Adapted material is
identified with its source and license; `CODE_OF_CONDUCT.md`, for example, is adapted from
Contributor Covenant 3.0 under CC BY-SA 4.0. Nothing here relicenses third-party work.
