# MetaphrasisWeb

The Metaphrasis website: the product page, the Privacy Policy and Terms of Use,
Support, plans and the release notes, at <https://metaphrasis.org/>. GitHub
Pages builds it with Jekyll, straight from `main`.

The app links to these paths, and a link compiled into a release stays in it,
so **they must never change**:

| Path | Page | Source |
|---|---|---|
| `/` | product page | `index.html` |
| `/privacy/` | Privacy Policy | `privacy.md` |
| `/terms/` | Terms of Use | `terms.md` |
| `/support/` | Support | `support.md` |
| `/plans/` | Free, Basic and Premium, with prices | `plans.md` |
| `/releases/` | release notes; `#1.0` jumps to a version | `releases.html` + `_data/releases.yml` |

The design reasons are in the app repository's
`docs/proposal-about-and-website.md`.

## Site facts

`_config.yml`, under `metaphrasis:`, holds the publisher, the contact address,
the governing law, the policies' effective date and the App Store link. The
pages read them from there and nowhere else. Two are still open: the App Store
link (empty shows "Coming soon"), and 1.0's date in `_data/releases.yml` (empty
shows "Upcoming").

The Privacy Policy and Terms are written from what the app, the SDK and the
Metaphrasis Cloud backend do. A change to any of them that touches data — a new
vendor, a new thing the server keeps, a retention period — changes the policy
in the same release. Have them read by someone qualified before publishing.

## Plans and prices

`plans.md` shows each plan's US price and what its week or month includes:
minutes of cloud speech, words translated, cloud voice. Those amounts are
copied by hand from the server's `METAPHRASIS_CLOUD_PRODUCTS` (the Metaphrasis
repository, `backend/`), and nothing keeps the two in step. When the server is
retuned, mirror it here in the same change. The feature rows follow the tier
table in the app repository's `docs/proposal-billing-tiers.md`.

## Publishing

In the repository's Settings › Pages, choose *Deploy from a branch*, `main`,
`/ (root)`. GitHub Pages serves a public repository free.

The site is served at the custom domain `metaphrasis.org`, named by the `CNAME`
file and by `url` in `_config.yml`, with *Enforce HTTPS* on. DNS:

| Name | Type | Value |
|---|---|---|
| `@` | A | `185.199.108.153` `185.199.109.153` `185.199.110.153` `185.199.111.153` |
| `@` | AAAA | `2606:50c0:8000::153` `2606:50c0:8001::153` `2606:50c0:8002::153` `2606:50c0:8003::153` |
| `www` | CNAME | `vladyslavc11.github.io` |
| `_github-pages-challenge-<owner>` | TXT | the domain verification GitHub shows |

GitHub redirects `www` and the old `vladyslavc11.github.io/MetaphrasisWeb/`
addresses to it. If the repository moves to another owner, verify the domain
again under that owner.

## Releasing a version

1. Add an entry at the top of `_data/releases.yml`. Its `version` is the app's
   `MARKETING_VERSION`, quoted.
2. Push. The app's "What's New in 1.1" opens `/releases/#1.1`.
3. Paste the same notes into App Store Connect.

When a policy changes, update its effective date in `_config.yml`, and mention
any change that matters in the release notes.

## Previewing locally

```sh
bundle install
bundle exec jekyll serve        # http://localhost:4000/
```

The `Gemfile` pins the Jekyll version GitHub Pages runs (3.10). It does not
use the `github-pages` gem itself, which does not install on Ruby 4.

