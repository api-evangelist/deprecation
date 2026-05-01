# API Deprecation Capabilities

Capabilities required to operate a disciplined API deprecation, sunset, and end-of-life program.

## Signaling Capabilities

- **Deprecation HTTP header** to mark a resource as deprecated.
- **Sunset HTTP header** (RFC 8594) to communicate the planned retirement timestamp.
- **Link relations** (`rel="sunset"`, `rel="successor-version"`, `rel="deprecation"`) to point at policy and migration documentation.
- **OpenAPI deprecation flags** on operations, parameters, headers, and schema properties.
- **AsyncAPI deprecation metadata** for events and channels.

## Communication Capabilities

- Developer portal banners and changelogs.
- Email and webhook notifications to subscribed consumers.
- Status page entries for active deprecations.
- In-product banners and SDK warnings.

## Lifecycle Stage Capabilities

- **Announced**: deprecation declared, no behavior change.
- **Deprecated**: header emitted, replacement available, traffic still served.
- **Sunset Scheduled**: removal date committed, Sunset header in effect.
- **Retired**: traffic refused with 410 Gone or redirected.
- **Removed**: route fully decommissioned.

## Consumer Impact Capabilities

- Consumption analytics by client, version, and endpoint.
- Direct outreach to top consumers of deprecated surfaces.
- Opt-in early adoption of replacement endpoints.
- Migration guides keyed to source and target versions.

## Governance Capabilities

- Public deprecation policy with stated notice windows.
- Approval workflow for declaring deprecation.
- Audit trail linking deprecations to product decisions.
- SLA for replacement availability before deprecation.

## Tooling Capabilities

- Linters that flag undocumented deprecations.
- Gateway plugins that inject Deprecation and Sunset headers.
- SDK generators that surface deprecation warnings to client developers.
- Dashboards tracking traffic decay against the sunset deadline.
