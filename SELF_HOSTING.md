# GitHub Profile Metrics — Current Setup

This repository is the source for the `subrojitroy10/subrojitroy10` profile README.

The profile deliberately separates **public presentation** from **private repository access**. Private repository names, source code, commit messages and other private content must never be written into this repository or exposed by a generated card.

## Current architecture

The profile currently uses three kinds of metrics:

1. **Primary GitHub stats** — rendered by the existing private deployment of `github-stats-extended` at `github-stats-extended-alpha.vercel.app`.
2. **Top languages** — rendered by the same private deployment.
3. **Contribution streak** — rendered by `streak-stats.demolab.com` from contribution activity visible on the GitHub profile.
4. **Profile views** — rendered by `komarev.com/ghpvc`.

The GitHub account has private-contribution visibility enabled. GitHub can therefore expose aggregate private contribution activity on the public contribution graph without exposing the underlying private repository identities or activity details.

## Why the primary stats deployment is self-hosted

The stats card uses:

```text
include_all_commits=true
```

The private deployment has its own GitHub API credentials and can therefore calculate aggregate statistics with access that a generic public card service would not have.

The README must never contain the token itself. Credentials belong only in the hosting provider's encrypted environment variables / secrets.

## Rank / grade marker

The rank indicator on the main GitHub stats card is enabled by leaving `hide_rank` unset (or setting it to `false`).

Do **not** add `hide_rank=true` unless the rank display is intentionally being removed.

## Streak card

The README currently uses:

```text
https://streak-stats.demolab.com?user=subrojitroy10&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D&mode=daily&timezone=Asia%2FKolkata
```

This provides total contribution / current streak / longest streak presentation similar to other high-signal GitHub profile READMEs.

A streak is only an activity indicator. It should not be described as a quality, productivity or engineering-performance score.

## Profile views

The visitor badge uses:

```text
https://komarev.com/ghpvc/?username=subrojitroy10
```

Treat this as a README/profile request counter rather than a unique-human analytics system.

## Credential guidance

If the self-hosted stats deployment ever needs to be recreated:

- Prefer the least-privileged token type and scopes supported by the deployed stats implementation.
- Only grant private-repository read access when it is actually required for aggregate private statistics.
- Store the token only in Vercel/GitHub encrypted secrets or environment variables.
- Never commit a PAT, token, `.env` file, Vercel environment dump or API response containing private repository metadata.
- Rotate the token immediately if it is ever printed in a log or committed.

Some GitHub stats implementations/forks have different support for fine-grained versus classic tokens, so verify the current upstream documentation before creating or rotating credentials rather than copying an old scope recipe.

## Future reliability upgrade

The next infrastructure improvement should be to generate the metric SVGs on a scheduled GitHub Actions workflow and commit/update only the generated SVG assets, for example:

```text
profile/
  stats.svg
  streak.svg
  languages.svg
```

The README would then reference local repository assets rather than depending on live image generation for every profile view.

Do not switch the primary private-aware stats card to a static workflow until the workflow's access model has been tested against the existing self-hosted card. The migration must not silently reduce private contribution coverage or expose private metadata.

## Validation after README changes

Before pushing profile changes:

1. Confirm `README.md` contains no secrets or private repository names that are not intended to be public.
2. Confirm the main stats URL does not contain `hide_rank=true` when the rank marker is expected.
3. Confirm the stats, languages, streak, typing and profile-view image endpoints return successfully.
4. Review the Git diff.
5. Push only after the working tree contains the intended profile/documentation changes.
