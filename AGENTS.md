# AGENTS.md

legend-depot is a fork of a FINOS project (finos/legend-depot) used for a delegated, supervised framework-upgrade demo. The default branch is pinned to upstream `901bae904c1a`; never sync it with upstream and never push to it directly — every change goes through a **draft pull request**.

## Toolchain
- JDK 17 (Temurin), Maven 3.9

## Build
```
mvn -q -DskipTests install
```

## Test
```
mvn -q test
```

## Rules
- Never edit anything under `.github/workflows/` (release/docker/publish workflows were intentionally removed in this fork).
- Never delete, `@Ignore`, or weaken tests to get a build green; document irreducible failures in the PR body instead.
- Touch only `pom.xml`, `CHANGELOG.md`, and the `src` files an upgrade requires.
