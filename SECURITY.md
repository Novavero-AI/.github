# Security policy

## Reporting a vulnerability

Report security issues privately: open the **Security** tab of the affected
repository and choose **Report a vulnerability**. Please do not open a public
issue for a security problem.

A useful report includes:

- the affected repository and version (`nova-nix --version`, the nova-cache
  version, or the install-nova-nix ref)
- the platform
- the smallest reproduction you have, such as the Nix expression, command or
  request that triggers it
- what an attacker gains

Fixes are made on the main branch, ship in the next release, and are
coordinated with the reporter before the details are public.

## Scope

Building a derivation runs its builder with your user's permissions, because
nova-nix has no build sandbox yet
([nova-nix#25](https://github.com/Novavero-AI/nova-nix/issues/25)). Running
code through a build is therefore expected, not a vulnerability.

These are vulnerabilities:

- evaluating a Nix expression that runs a command of the expression's
  choosing, or writes to a path of its choosing outside the store
- a substituter, a cache server or a NAR reader that accepts content its
  signatures or hashes do not cover
- the install-nova-nix action installing anything other than the release
  archive it verified
