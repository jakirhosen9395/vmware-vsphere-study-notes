# ESXi Commands Cheatsheet

Quick reference for common ESXi command-line operations.

## System Information

### Get ESXi version
```bash
vmware -vl
```

### Get hardware info
```bash
esxcli hardware platform get
esxcli hardware cpu list
esxcli hardware memory get
```

### Check uptime
```bash
esxcli system stats uptime get
```

## Host Management

### Restart host services
```bash
/etc/init.d/hostd restart
/etc/init.d/vpxa restart
```

### Enable/Disable SSH
```bash
vim-cmd hostsvc/enable_ssh
vim-cmd hostsvc/disable_ssh
```

### Enable/Disable ESXi Shell
```bash
vim-cmd hostsvc/enable_esx_shell
vim-cmd hostsvc/disable_esx_shell
```

### Put host in maintenance mode
```bash
esxcli system maintenanceMode set --enable true
esxcli system maintenanceMode set --enable false
```

### Reboot/Shutdown host
```bash
esxcli system shutdown reboot -r "Reason for reboot"
esxcli system shutdown poweroff -r "Reason for shutdown"
```

## Virtual Machine Management

### List all VMs
```bash
vim-cmd vmsvc/getallvms
esxcli vm process list
```

### Power operations
```bash
# Power on VM (use VM ID from getallvms)
vim-cmd vmsvc/power.on <VMID>

# Power off VM
vim-cmd vmsvc/power.off <VMID>

# Reset VM
vim-cmd vmsvc/power.reset <VMID>

# Shutdown guest OS
vim-cmd vmsvc/power.shutdown <VMID>
```

### Snapshot management
```bash
# List snapshots
vim-cmd vmsvc/snapshot.get <VMID>

# Create snapshot
vim-cmd vmsvc/snapshot.create <VMID> "snapshot_name" "description" 0 0

# Remove snapshot
vim-cmd vmsvc/snapshot.remove <VMID>
```

### Kill VM process (force power off)
```bash
esxcli vm process kill --type=force --world-id=<WorldID>
```

## Networking

### List virtual switches
```bash
esxcli network vswitch standard list
esxcli network vswitch dvs vmware list
```

### List VMkernel adapters
```bash
esxcli network ip interface list
esxcli network ip interface ipv4 get
```

### List port groups
```bash
esxcli network vswitch standard portgroup list
```

### Add VMkernel adapter
```bash
esxcli network ip interface add --interface-name=vmk1 --portgroup-name=vMotion
esxcli network ip interface ipv4 set --interface-name=vmk1 --ipv4=192.168.1.10 --netmask=255.255.255.0 --type=static
```

## Storage

### List datastores
```bash
esxcli storage filesystem list
esxcli storage vmfs extent list
```

### Rescan storage adapters
```bash
esxcli storage core adapter rescan --all
```

### List storage adapters
```bash
esxcli storage core adapter list
```

### List VMFS volumes
```bash
esxcli storage vmfs extent list
```

### Mount NFS datastore
```bash
esxcli storage nfs add --host=nfs.example.com --share=/export/datastore1 --volume-name=NFS-Datastore1
```

## Logs

### Tail logs in real-time
```bash
tail -f /var/log/vmkernel.log
tail -f /var/log/hostd.log
tail -f /var/log/vpxa.log
```

### View log files
```bash
cat /var/log/vmkernel.log
less /var/log/hostd.log
```

### Key log locations
```
/var/log/vmkernel.log        # VMkernel events
/var/log/hostd.log           # Host daemon
/var/log/vpxa.log            # vCenter agent
/var/log/vobd.log            # VMware Observation
/var/log/fdm.log             # HA logs
/var/log/vmware/hostd/       # Additional hostd logs
```

## Licensing

### View license information
```bash
vim-cmd vimsvc/license --show
```

### Add license key
```bash
vim-cmd vimsvc/license --set XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
```

## User Management

### List users
```bash
esxcli system account list
```

### Add user
```bash
# Note: Use -p to prompt for password securely instead of specifying in command
esxcli system account add -d "Description" -i <username> -p
# Or specify password directly (not recommended for production)
esxcli system account add -d "Description" -i <username> -p <password>
```

### Remove user
```bash
esxcli system account remove -i <username>
```

## Firewall

### List firewall rules
```bash
esxcli network firewall ruleset list
```

### Enable/disable ruleset
```bash
esxcli network firewall ruleset set --ruleset-id=<ruleset> --enabled=true
esxcli network firewall ruleset set --ruleset-id=<ruleset> --enabled=false
```

### Common rulesets
- `sshServer` - SSH access
- `vMotion` - vMotion traffic
- `NFS` - NFS client
- `iSCSI` - iSCSI traffic

## Troubleshooting

### Generate support bundle
```bash
vm-support
```

### Test network connectivity
```bash
vmkping -I vmk0 192.168.1.1
vmkping -d -s 8972 <destination_IP>  # Test jumbo frames
```

### View running processes
```bash
esxcli vm process list
ps | grep vmx
```

### Check hardware sensors
```bash
esxcli hardware ipmi sdr list
```

---

**Note**: Always test commands in a lab environment before using in production. Some commands require the host to be in maintenance mode.
