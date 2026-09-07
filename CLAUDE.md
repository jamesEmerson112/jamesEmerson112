# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is the GitHub profile README repository for the `jamesEmerson112` account. Because the repository name matches the account name, GitHub renders `README.md` at the top of https://github.com/jamesEmerson112. The content is `README.md` plus one GitHub Actions workflow that regenerates the stats image. There is no source code, build system, linter, or test suite, so there are no build or test commands. Verification means rendering the Markdown and checking the links.

## Working on the README

The README is written for recruiters hiring for AI/ML engineering roles, and it follows the shape of established ML practitioners' profiles: one present-tense sentence about what James builds, one sentence per featured repo carrying its strongest number, and a total length of one or two screens. Detail belongs in each repo's own README, which is where a recruiter clicks through. A featured repo with a live deployment gets a trailing "Live:" link. Its sections run in this order: a header with a positioning sentence and contact badges, "Now", "Featured work" with the sub-sections ML training and evaluation, Georgia Tech coursework, Hackathons, and Rust track and open source, then "Languages and tools", "GitHub stats", and "Beyond code". A repository appears in only one sub-section. Technical sections stay above "Beyond code", which holds the personal lines and should be kept as they are.

Only public repositories get links, because a private repository link returns a 404 for a visitor. Check with `gh repo view jamesEmerson112/<name> --json isPrivate` before adding one. Private work is described in one unlinked clause or left out. Never link a repository that mainly holds graded coursework solutions; the public, solution-free companions such as `backprop-by-hand` are the ones to link. Forks are featured only when the account has original commits in them, and the link should go where the contribution is visible.

Every project claim in the README was taken from that repository's own README or files, and self-reported numbers are labelled as such (an open pull request is not a leaderboard placement). When adding or changing a claim, find the supporting text in the repository first, and never state a result, placement, or date the repository does not state.

GitHub sanitizes README HTML. Stay within `h1` to `h6`, `p`, `img`, `a`, `b`, `strong`, `em`, `br`, lists, and the attributes `src`, `href`, `alt`, `width`, `height`, and `align`. Inline `style` attributes, `<style>`, and `<script>` are stripped silently. Markdown headings are used for every section after the header.

Badges are shields.io images. Contact badges use `style=flat-square` in the Markdown link form `[![alt](badge-url)](target-url)`, with exactly one pair of parentheses around the target. The "Languages and tools" wall uses bare `<img>` tags with `style=for-the-badge` and an `alt` attribute. The `logo` parameter must be a current Simple Icons slug; LinkedIn, Java, and C# no longer have one, so those badges carry no logo, and the CSS slug is `css`, not `css3`. The "GitHub stats" section is a single image, `github-metrics.svg`, generated inside this repository by the workflow in `.github/workflows/metrics.yml` (lowlighter/metrics, daily at 12:00 UTC, also on manual dispatch). The workflow needs a repository secret named `METRICS_TOKEN` holding a classic personal access token with no scopes; fine-grained tokens are rejected by the action, and the default `GITHUB_TOKEN` cannot read user-level data. The action commits the SVG back with a "[Skip GitHub Action]" marker, so do not add a push trigger on the SVG path. Third-party stats hosts (github-readme-stats, summary cards) were tried first and dropped because the public github-readme-stats deployment was returning HTTP 503 in September 2026.

To preview rendering without pushing, use GitHub's own renderer:

```
gh api markdown -F text=@README.md -f mode=gfm -f context=jamesEmerson112/jamesEmerson112
```

To check links, extract every URL and request each with `curl -sIL -o /dev/null -w '%{http_code}'`, expecting 200.

The history is one small "Update README.md" commit per content change, several made through the GitHub web editor. Keep that granularity.
