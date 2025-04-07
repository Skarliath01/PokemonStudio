
# Security Policy

## Supported Versions

We currently support the latest stable release of the project.

| Version | Supported |
|---------|-----------|
| 0.1.x   | ✅         |

---

## Reporting a Vulnerability

If you discover a security vulnerability, please open an issue and tag it as `security`.

For critical vulnerabilities, you may contact the maintainers directly.

---

## Known Vulnerabilities (as of initialization)

The project uses [Create React App](https://create-react-app.dev/) and `react-scripts@5.0.1`, which currently includes some indirect vulnerabilities reported by `npm audit`. These include:

- `nth-check` (via `svgo`)
- `css-select`
- `postcss`
- `resolve-url-loader`

These are:
- Limited to the build/dev toolchain
- Not exploitable in production runtime
- Tracked upstream by the `react-scripts` maintainers

We monitor these and will update `react-scripts` when a patched version is available.

---

## Recommendations

If you build production versions of this project:
- Run `npm audit` regularly
- Keep dependencies up to date
- Do not expose development containers publicly
