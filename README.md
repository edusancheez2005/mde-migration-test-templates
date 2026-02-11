# MDE/XDR Migration Test Templates

This repo contains **sample ARM templates** with legacy Microsoft Defender APIs for testing migration scanners.

## What's Here

| Folder | Description | Legacy APIs Used |
|--------|-------------|------------------|
| `playbooks/isolate-machine/` | Isolate a device | `api.securitycenter.microsoft.com/api/machines/{id}/isolate` |
| `playbooks/run-hunting-query/` | Advanced hunting | `api.security.microsoft.com/api/advancedqueries/run` |
| `playbooks/get-alerts/` | Get security alerts | `api.securitycenter.microsoft.com/api/alerts` |
| `playbooks/get-incidents/` | Get incidents | `api.security.microsoft.com/api/incidents` |
| `connectors/` | Legacy connector definitions | `MicrosoftDefenderATP`, `shared_windowsdefenderatp` |

## Migration Status

These APIs are being **retired February 1, 2027**. Migrate to:
- **Microsoft Graph Security API** (`graph.microsoft.com/beta/security/...`)

## Testing

Use the scanner at: [API_Migration tools]
```bash
python scan_templates.py
# Enter this repo URL when prompted
```
