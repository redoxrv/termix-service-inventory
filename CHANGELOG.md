# Changelog

## 0.6.1

### Fixed

- Omit an empty Dokploy routers section so Traefik accepts private access configuration.
- Preserve existing access history while upgrading the previous public-state baseline.

## 0.6.0

### Added

- Register HTTP services on approved guests without publishing them.
- Opt in to Internet/Tailscale access for the Dokploy administration panel using its private API.
- Preserve exact routing snapshots and recover uncertain writes after a process restart.
- Choose Internet, Tailscale only or unpublished access with a reviewed plan.
- Require an explicit public hostname only when enabling Internet access.

## 0.5.0

### Changed

- Group services by machine and keep current access separate from requested changes.
- Display protected infrastructure endpoints using explicit sanitized metadata.
- Keep source freshness and reachability evidence independent.

### Added

- Restore filtered Proxmox cache during a reviewed upgrade without changing its original timestamp.

## 0.4.0

### Added

- Read VM/LXC metadata directly through a dedicated read-only Proxmox API token.
- Show independent source availability and keep unrelated inventory usable during outages.
- Control pre-registered HTTP services through a separate HTTPS access controller.
- Prepare revision-bound plans, apply access and restore previous routing with backend permissions and audit.

### Security

- Verify the token has only Sys.Audit and VM.Audit throughout its effective permissions.
- Allow private HTTPS only for the exact configured Tailscale hostname, with verified TLS and no redirects.
- Bind executable plans and operations to the acting user and configured controller; preserve idempotent retries.
- Keep configuration/backend checks separate from unverified external network reachability.

## 0.3.0

### Added

- Include filtered VM/LXC snapshots from explicit native Proxmox discovery.
- Distinguish machines from Docker containers and show snapshot freshness.
- Save requested access profiles for guest services without exposing a whole guest.
- Require a separate backend permission to refresh metadata; reject secrets, stale imports and unsafe identities.

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
