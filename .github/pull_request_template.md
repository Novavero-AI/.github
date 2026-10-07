<!--
What this changes and why. For a behavior change, say what upstream Nix does
and how you checked. Link the issue it resolves with "Closes #N".
-->

- [ ] User-visible changes have a changelog entry where the repository keeps
      one (a `changelog.d/` fragment in nova-nix, `CHANGELOG.md` in nova-cache)
- [ ] The repository's CI gate passes locally (for nova-nix:
      `cabal build --enable-tests --ghc-options="-Werror"`, then `cabal test`)
