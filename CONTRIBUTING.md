# Contributing to awesome-te

Thanks for helping keep this the best map of Teenage Engineering hacking work. The bar is
**curate, don't collect**: every entry should be something you would actually recommend to another
hacker, with a clear reason it belongs.

## What qualifies

An entry must be:

- **TE-specific** - a project for a real Teenage Engineering device (SP-1, TP-7, OP-1/field, OP-Z,
  OP-XY, EP-133 K.O. II, EP-1320, Pocket Operators, TX-6, etc.).
- **Real and reachable** - a public URL that works (repo, site, forum thread, hackaday project).
- **Usable today** - you can actually get and run or read it right now. No announced-but-unreleased
  projects, no "coming soon," no private repos.
- **Useful for the gear** - custom firmware, reverse engineering, tools/software, hardware mods,
  cases/accessories, teardown/recovery, or a community hub. Free or paid, open or commercial - just a
  real, working thing for a real device, not a low-effort ad.

When in doubt, leave it out. A short, trustworthy list beats a long one.

## How to add an entry

1. Edit `README.md`.
2. Find the right **device** section, then the right **job-to-be-done** sub-heading
   (Custom firmware & OS / Reverse engineering & docs / Tools & software / Hardware mods /
   Teardown, flashing & recovery / Community). Add the sub-heading if it does not exist yet.
3. Add one line, keeping the section in a sensible order:

   ```
   - 🟢 [Name](https://example.com) - One sentence on why it matters, ending with a period.
   ```

4. Update the Table of Contents if you added a new section.
5. Open a pull request.

## Entry style (kept lint-clean)

- One line per entry: `- 🟢 [Name](url) - description.`
- Description: a single sentence, sentence case, **ending with a period**, roughly 20 words or less,
  saying *why it matters* (not just what it is).
- URLs: **no trailing slash** (`https://op1.fun`, not `https://op1.fun/`).
- **Status emoji** - start every entry with one status marker, right after the `- `, so readers can
  scan the list at a glance:
  - 🟢 **active** - a commit, release, or update in the last 12 months.
  - 🟡 **dormant** - no commits, releases, or updates in 12+ months, but still works.
  - 🔴 **archived** - read-only / explicitly archived.

  Be honest - half of any niche hardware scene is dormant, and saying so is what keeps this list
  trustworthy. Sort each subsection 🟢 first.

## Removing / fixing

- Dead links are caught automatically by the weekly link-check workflow, which opens an issue.
- If a link moved, **fix it**. If the project still resolves but is read-only or closed, **mark it
  🔴 archived** - a known-dead pointer is often still useful history. If the project is gone entirely
  (the URL 404s), remove the entry; git history keeps the record. Otherwise remove only true
  duplicates or spam.

## License

Contributions are released under [CC0 1.0](LICENSE) (public domain). By contributing you agree to
release your contribution under CC0.
