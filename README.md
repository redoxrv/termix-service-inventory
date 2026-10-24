# Service Inventory for Termix

Signed generic Dokploy, Docker and Proxmox inventory grouped by machine.
Current configured access is separate from requested changes. No deployment
inventory, credentials or private configuration is shipped.

Registry: `https://raw.githubusercontent.com/redoxrv/termix-service-inventory/main/index-v3.json`
Signing fingerprint: **`b9479b0c9d7d55d4`**. Public key: `IbfaK9qPsrVvKjY1Z5biFV+v0d8x0+xGA8zATnAB6vY=`.

Keep signature verification and exact version pins enabled, with automatic
updates disabled. Versions 0.6.3, 0.6.2, 0.6.1, 0.6.0, 0.5.0 and 0.4.0 remain available from immutable
artifact commits. Use the supported update API to preserve plugin-owned data;
uninstall removes that data and is not an upgrade procedure.

HTTP registration, Internet/Tailscale/unpublished routing and rollback require
an authenticated independent access controller with an approved guest catalog.
Disabled routes have no application upstream; a provisioned private listener may
remain as an inert 404. Existing listeners, DNS, host firewall and public ingress
must be provisioned and independently qualified by the administrator.

Native Dokploy administration controls are an explicit backend opt-in. They
change only the validated Dokploy public routers while preserving the private
management API. This provider supports public and Tailscale modes. Its upstream
API has no atomic compare-and-swap; the plugin serializes its own requests,
checks hashes and preserves recovery data, but cannot lock external editors.

Configuration/backend checks do not prove external Internet or tailnet access.
The original registries, public keys and signed artifacts remain unchanged.
License: Apache-2.0; third-party attribution is included in NOTICE.
