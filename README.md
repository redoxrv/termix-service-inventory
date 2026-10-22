# Service Inventory for Termix

Signed distribution of a generic Termix plugin for Dokploy applications,
Compose services and containers. Compatible with Termix 26.10.4+ and Plugin API 1.11.

This repository contains the plugin package, registry index, public verification
key and license notices. It contains no installation addresses, credentials,
inventory, backups or deployment configuration. The package includes readable
program code and source maps.

## Install

Add this custom registry in Termix → Plugins → Registries:

`https://raw.githubusercontent.com/redoxrv/termix-service-inventory/main/index.json`

Compare the signing key ID before trusting the registry:

**`6ed423a160951f7c`**

Public key: `zZFemt0hwuX9oXcKrchftT9Si1EsBkqltUxouH9IuxY=`

Install **Service Inventory**, then configure the Dokploy API origin, a dedicated
service API key and an optional node label in the central plugin's administrator
settings. Linked desktop apps use the central controller.

## What it does

- Discovers applications, Compose services and containers while the tab is open.
- Shows configuration-derived exposure, freshness and explicit unknown states.
- Saves desired access profiles and prepares plans with backend permission checks.

Version 0.2.0 does not execute exposure changes. It never publishes services,
changes firewall rules, opens SSH connections or reads container environment
variables. The package has no telemetry or instance-specific defaults.

Termix plugins run in-process: signatures establish origin and integrity, not
sandbox isolation. Review the package and keep signature verification enabled.
The API key inherits its actual Dokploy privileges; the plugin limits its own
requests to inventory GET operations.

License: Apache-2.0. Bundled third-party notices are in [NOTICE](NOTICE).
