# abcdesign.app

This repository publishes [abcdesign.app](https://abcdesign.app), the page where a team edits its brief together, live, for any abcd-managed repository.

It holds no code of its own. The page is written by [abcd](https://github.com/intentdriven/abcd) itself, with `abcd session page`. The workflow here builds it from the latest abcd release and deploys it to this repository's GitHub Pages:

- **When:** daily, or when started by hand.
- **Checks:** the release binary is checked against the release's checksums and its build provenance before it runs.
- **Credentials:** none beyond the short-lived token GitHub gives each run.

A team's session runs on the team's own relay, never on anything abcd runs (see `abcd session serve` and `abcd session blueprint`). A change to the page is made in abcd and reaches this site with the next abcd release.
