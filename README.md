# MetaphrasisWeb

The Metaphrasis website: the product page, the Privacy Policy and Terms of Use,
Support, and the release notes. GitHub Pages builds it with Jekyll, straight
from `main`.

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

## Placeholders

Every choice not yet made is a `[TBD: …]` value in `_config.yml`, under
`metaphrasis:`: publisher, contact email, governing law, the policies' effective
date and the App Store link. The pages read these from there and nowhere else.
The release date of 1.0 is in `_data/releases.yml`.

```sh
grep -rn "TBD" --include="*.yml" --include="*.md" --include="*.html" .
```

The Privacy Policy and Terms are drafts written from what the app does. Have
them read by someone qualified before publishing.

## Plans and prices

`plans.md` shows each plan's US price and what its week or month includes:
minutes of cloud speech, words translated, cloud voice. Those amounts are
copied by hand from the server's `METAPHRASIS_CLOUD_PRODUCTS` (the Metaphrasis
repository, `backend/`), and nothing keeps the two in step. When the server is
retuned, mirror it here in the same change. The feature rows follow the tier
table in the app repository's `docs/proposal-billing-tiers.md`.

## Publishing

In the repository's Settings › Pages, choose *Deploy from a branch*, `main`,
`/ (root)`. GitHub Pages serves a public repository free. The site is then at
<https://vladyslavc11.github.io/MetaphrasisWeb/>.

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
bundle exec jekyll serve        # http://localhost:4000/MetaphrasisWeb/
```

The `Gemfile` pins the Jekyll version GitHub Pages runs (3.10). It does not
use the `github-pages` gem itself, which does not install on Ruby 4.

## Moving to a custom domain

1. Set `url` to the domain and `baseurl` to `""` in `_config.yml`.
2. Add a `CNAME` file containing the domain.
3. Point the domain's DNS at GitHub Pages, and turn on *Enforce HTTPS*.
4. In the same app release, change `AppLinks.site`.

The paths stay the same.
