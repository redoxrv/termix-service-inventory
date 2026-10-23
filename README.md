# Service Inventory for Termix

Signed generic distribution for Dokploy, Docker and Proxmox inventory, with
registered HTTP service access through a separate controller. Credentials,
deployment configuration, inventory and backups are not included.

## Version 0.4.0

Add this separate registry and compare its signing fingerprint:

`https://raw.githubusercontent.com/redoxrv/termix-service-inventory/main/index-v2.json`

**`b9479b0c9d7d55d4`**

Public key: `IbfaK9qPsrVvKjY1Z5biFV+v0d8x0+xGA8zATnAB6vY=`

Configure inventory sources and the access controller on the central server.
Linked desktop apps use the same controller. Registered service changes require
a fresh plan, administrative permission and revision checks. Configuration and
backend checks do not claim independent Internet or Tailscale reachability.

## Earlier installations and rollback

The original registry remains unchanged at:

`https://raw.githubusercontent.com/redoxrv/termix-service-inventory/main/index.json`

Original signing fingerprint: **`6ed423a160951f7c`**. Its 0.2.0 package and signature
are preserved. On Termix26.10.4 a registry cannot change its pinned signing key
in place. Migrating an installed plugin to the separate registry requires a
qualified current data backup and preservation of its settings before reinstall.
Uninstall removes plugin-owned data; review any stored data before proceeding.

Packages contain readable program code and source maps. Signatures establish
origin and integrity, rather than sandbox isolation. Keep signature verification
enabled. License: Apache-2.0; bundled third-party attribution is in NOTICE.
