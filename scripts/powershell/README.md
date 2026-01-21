# PowerShell Scripts

This directory contains PowerShell and PowerCLI scripts for VMware vSphere management.

## Script Categories

### VM Management
- VM creation and configuration
- Template management
- Bulk VM operations
- VM inventory reporting

### vCenter Management
- vCenter configuration
- Permission management
- Resource pool management
- Cluster operations

### Automation
- Deployment automation
- Migration scripts
- Backup automation
- Compliance checking

### Reporting
- Inventory reports
- Performance reports
- Capacity planning
- License tracking

## Prerequisites

Install VMware PowerCLI:
```powershell
Install-Module -Name VMware.PowerCLI -Scope CurrentUser
```

## Usage

Connect to vCenter before running scripts:
```powershell
Connect-VIServer -Server vcenter.example.com
```

## Best Practices

1. Test in lab environment first
2. Use PowerCLI cmdlets when available
3. Implement proper error handling
4. Don't hardcode credentials (use secure methods)
5. Include help documentation in scripts
6. Follow PowerShell naming conventions

## Example Scripts

Add your PowerShell scripts here:
- `New-BulkVMs.ps1`
- `Get-VMInventoryReport.ps1`
- `Set-VMResourceAllocation.ps1`
- `Export-VMTemplates.ps1`
- `Get-vCenterHealthCheck.ps1`
