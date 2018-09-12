- https://yarnpkg.com/en/docs/dependency-versions
- https://semver.npmjs.com/

# Caret Ranges

Allow changes that do not modify the first non-zero digit in the version,
either the `3` in `3.1.4` or the `4` in `0.4.2`.

| Version range | Expanded version range |
| ------------- | ---------------------- |
| `^3.1.4`      | `>=3.1.4 <4.0.0`       |
| `^0.4.2`      | `>=0.4.2 <0.5.0`       |
| `^0.0.2`      | `>=0.0.2 <0.0.3`       |

If part of the version is left out, the missing parts are filled in with
zeroes. However, they will still allow for that value to be changed.

| Version range | Expanded version range |
| ------------- | ---------------------- |
| `^0.0.x`      | `>=0.0.0 <0.1.0`       |
| `^0.0`        | `>=0.0.0 <0.1.0`       |
| `^0.x`        | `>=0.0.0 <1.0.0`       |
| `^0`          | `>=0.0.0 <1.0.0`       |

# Tilde Ranges

Using `~` with a minor version specified allows `patch` changes. Using `~` with
only major version specified will allow `minor` changes.

| Version range | Expanded version range      |
| ------------- | --------------------------- |
| `~3.1.4`      | `>=3.1.4 <3.2.0`            |
| `~3.1`        | `3.1.x` or `>=3.1.0 <3.2.0` |
| `~3`          | `3.x` or `>=3.0.0 <4.0.0`   |