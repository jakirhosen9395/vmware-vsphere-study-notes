# Scripts

This directory contains automation scripts for VMware vSphere management.

## Structure

- **bash/**: Shell scripts for Linux/ESXi automation
- **powershell/**: PowerCLI and PowerShell scripts for vSphere management

## Bash Scripts

Located in the `bash/` subdirectory. Examples:
- ESXi configuration scripts
- Backup automation
- Log collection
- Health check scripts
- Deployment automation

## PowerShell Scripts

Located in the `powershell/` subdirectory. Examples:
- PowerCLI scripts for VM management
- Bulk operations (create, delete, configure VMs)
- Reporting scripts
- vCenter automation
- Migration scripts

## Usage Guidelines

1. **Always test in a lab environment first**
2. Review scripts before running in production
3. Backup your environment before making changes
4. Document any customizations
5. Follow security best practices (don't hardcode credentials)

## Prerequisites

### For Bash Scripts
- SSH access to ESXi hosts
- Appropriate permissions
- Required tools installed (esxcli, vim-cmd, etc.)

### For PowerShell Scripts
- PowerCLI module installed
- vCenter/ESXi credentials
- Appropriate permissions

## Contributing

When adding scripts:
- Include comments explaining functionality
- Add usage examples in the header
- Test thoroughly before committing
- Follow coding standards for the language
