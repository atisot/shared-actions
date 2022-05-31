# shared-actions

- [CI (Node.js)](#ci-nodejs) – Test & Lint for Node.js apps
- [CI (Java Gradle)](#ci-java-gradle) – Build for Java Gradle apps
- [Release (MC Mod)](#release-mc-mod) – Release for Minecraft Mods

---

## CI (Node.js)

| OPTION       | TYPE                        |
|--------------|-----------------------------|
| node-version | ?number (default: `16`)     |
| setup-redis  | ?boolean (default: `false`) |

```yaml
jobs:
  ci:
    uses: atisot/shared-actions/.github/workflows/ci-nodejs.yml@v1.2.0
```

---

## CI (Java Gradle)

| OPTION       | TYPE                                 |
|--------------|--------------------------------------|
| java-version | number                               |
| distribution | ?string (default: `temurin`)         |
| command      | ?string (default: `./gradlew build`) |

```yaml
jobs:
  ci:
    uses: atisot/shared-actions/.github/workflows/ci-java-gradle.yml@v1.2.0
    with:
      java-version: 17
```

---

## Release (MC Mod)

| OPTION       | TYPE                                 |
|--------------|--------------------------------------|
| java-version | number                               |
| distribution | ?string (default: `temurin`)         |
| command      | ?string (default: `./gradlew build`) |

```yaml
jobs:
  release:
    uses: atisot/shared-actions/.github/workflows/release-mc-mod.yml@v1.2.0
    with:
      java-version: 17
```
