# Service Inventory for Termix

Signed generic Dokploy, Docker and Proxmox inventory with a compact machine and
service view. Current configured access is separate from requested changes.
Administrative endpoints can be declared through sanitized backend metadata;
protected administration may be public or private. No deployment data is shipped.

## Registry

`https://raw.githubusercontent.com/redoxrv/termix-service-inventory/main/index-v3.json`

Signing fingerprint: **`b9479b0c9d7d55d4`**. Public key: `IbfaK9qPsrVvKjY1Z5biFV+v0d8x0+xGA8zATnAB6vY=`.
Keep signature verification enabled. The index lists versions 0.5.0 and 0.4.0;
each artifact URL is pinned to an immutable commit. Installed versions should
remain explicitly pinned with automatic updates disabled.

Termix 26.10.4 cannot change the source of an installed plugin through its API.
Moving from an older registry requires a qualified full data backup, an exact
review of plugin-owned data, and preservation of settings before reinstalling.
Uninstall always removes owned data. Do not blindly reinstall a populated plugin.
Once installed from this registry, the normal update API can switch between its
signed versions without uninstalling. Review state and any migrations first.

HTTP access controls apply only to services registered with an independent
controller. Port/domain onboarding and an unpublished target are not implemented
by this UI update. Inventory never changes exposure. Configuration and backend
checks do not prove independent WAN or Tailscale reachability.

The original registries, keys and signed 0.2.0/0.4.0 artifacts remain unchanged.
License: Apache-2.0; third-party attribution is included in NOTICE.
