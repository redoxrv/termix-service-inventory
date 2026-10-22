# Changelog

## 0.2.0

### Changed

- Generic Service Inventory identity and configurable HTTPS Dokploy origins.
- Neutral defaults and documentation without installation-specific information.

### Security

- Bounded inventory responses, total request deadlines and strict origin validation.
- Protected administration services reject desired-profile writes.
- Distribution contains no instance addresses, account references or runtime data.

## 0.1.0

### Added

- Automatic Dokploy application and container inventory with refresh while visible.
- Configuration-derived exposure, freshness, protected administration and explicit unknown states.
- Central controller transport for linked desktop clients, without copying the Dokploy token.
- Desired access profiles and non-executing plans, with permission checks and audit.

### Security

- No automatic exposure, Docker socket, SSH credentials, container environment exports or arbitrary API routes.
- Public/private execution remains unavailable until its dedicated executor and verification are qualified.
