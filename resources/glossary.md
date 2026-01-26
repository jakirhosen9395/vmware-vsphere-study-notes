# VMware vSphere Glossary

A comprehensive glossary of VMware vSphere and virtualization terminology.

## A

**Admission Control**
- vSphere HA feature that ensures sufficient resources are available for VM failover in the event of host failure.

**Affinity Rules**
- DRS rules that keep specified VMs together on the same host or separate hosts.

**Anti-Affinity Rules**
- DRS rules that keep specified VMs on different hosts for redundancy.

## B

**Ballooning**
- Memory reclamation technique where the hypervisor uses a driver in the guest OS to reclaim memory.

**Blue Screen of Death (BSOD)**
- Critical system error in Windows, often referred to as a Purple Screen of Death (PSOD) in ESXi.

## C

**Clone**
- An exact copy of a virtual machine created from either a VM or template.

**Cluster**
- A collection of ESXi hosts that share resources and can be managed as a single entity.

**Cold Migration**
- Moving a powered-off VM from one host or datastore to another.

**Content Library**
- Repository for VM templates, vApps, and other files that can be shared across vCenter instances.

## D

**Datacenter**
- Logical container in vCenter that holds hosts, clusters, resource pools, and VMs.

**Datastore**
- Storage location for VM files, ISOs, and templates (can be VMFS, NFS, vSAN, or vVols).

**Distributed Port Group**
- Network port group configuration on a vSphere Distributed Switch that spans multiple hosts.

**Distributed Resource Scheduler (DRS)**
- Feature that balances computing workloads across hosts in a cluster using vMotion.

**Distributed Switch (vDS)**
- Virtual switch that spans multiple ESXi hosts, managed centrally through vCenter.

## E

**Enhanced vMotion Compatibility (EVC)**
- Feature that ensures vMotion compatibility between hosts with different CPU generations.

**ESXi**
- VMware's bare-metal hypervisor that runs directly on physical hardware.

**ESXCLI**
- Command-line interface for managing ESXi hosts.

## F

**Fault Tolerance (FT)**
- vSphere feature providing continuous availability by creating a live shadow VM instance.

**Folder**
- Organizational container in vCenter for grouping VMs, hosts, datastores, or networks.

## G

**Guest OS**
- Operating system running inside a virtual machine.

**Guest Customization**
- Process of customizing a guest OS during VM deployment (hostname, IP, domain join, etc.).

## H

**HA (High Availability)**
- Feature that automatically restarts VMs on other hosts if a host fails.

**Host**
- Physical server running ESXi hypervisor.

**Host Profile**
- Template for ESXi host configuration that ensures consistency across multiple hosts.

**Hot-Add**
- Ability to add CPU or memory resources to a running VM without powering it off.

**Hypervisor**
- Software layer that creates and manages virtual machines (ESXi is a Type 1 hypervisor).

## I

**iSCSI**
- Internet Small Computer Systems Interface; protocol for linking data storage over IP networks.

**ISO**
- Disk image file format used for installing operating systems and software.

## L

**Linked Clone**
- VM clone that shares virtual disks with the parent VM to save storage space.

**Lockdown Mode**
- Security feature that restricts direct access to ESXi hosts, requiring all access through vCenter.

**LUN (Logical Unit Number)**
- Logical representation of a storage volume presented to ESXi hosts.

## M

**MAC Address**
- Media Access Control address; unique identifier for network interfaces.

## N

**NFS (Network File System)**
- File-level storage protocol used for datastores.

**NIC (Network Interface Card)**
- Physical or virtual network adapter.

**NIC Teaming**
- Combining multiple network adapters for redundancy and load balancing.

## O

**OVF (Open Virtualization Format)**
- Open standard for packaging and distributing virtual appliances.

**OVA (Open Virtual Appliance)**
- Single-file OVF package containing all VM files.

## P

**Port Group**
- Logical grouping of virtual machine network ports with common configuration.

**PowerCLI**
- VMware's PowerShell-based command-line interface for automation.

**PSOD (Purple Screen of Death)**
- Critical error screen in ESXi, equivalent to Windows BSOD.

## R

**Resource Pool**
- Logical abstraction for flexible management of CPU and memory resources.

**Reservation**
- Guaranteed minimum amount of CPU or memory allocated to a VM.

## S

**Shares**
- Relative priority for resource allocation among VMs competing for resources.

**Snapshot**
- Point-in-time copy of a VM's state, including disk, memory, and configuration.

**Storage DRS (SDRS)**
- Feature that balances storage workloads across datastores in a datastore cluster.

**Storage vMotion**
- Migrating a VM's virtual disks between datastores while the VM remains running.

**Standard Switch (vSS)**
- Virtual switch configured and managed independently on each ESXi host.

## T

**Template**
- Master copy of a VM used for deploying multiple similar VMs.

**Thin Provisioning**
- Storage allocation method where disk space is allocated on-demand rather than upfront.

**Thick Provisioning**
- Storage allocation method where all disk space is allocated immediately.

**Transparent Page Sharing (TPS)**
- Memory optimization technique that eliminates duplicate memory pages.

## V

**vApp**
- Container for one or more VMs that can be managed as a single entity.

**vCenter Server**
- Centralized management platform for ESXi hosts and VMs.

**vCenter Server Appliance (VCSA)**
- Linux-based vCenter Server deployment (recommended over Windows).

**vDS (vSphere Distributed Switch)**
- See Distributed Switch.

**Virtual Disk (VMDK)**
- File format for virtual machine hard disks.

**Virtual Hardware**
- Virtualized computer components (CPU, memory, disk, network) presented to VMs.

**Virtual Machine (VM)**
- Software-based computer running an operating system and applications.

**VM-to-VM Affinity**
- DRS rule keeping specified VMs together on the same host.

**VMFS (Virtual Machine File System)**
- VMware's clustered file system for storing VM files.

**VMkernel**
- Core component of ESXi that manages resources and provides services.

**VMkernel Port**
- Virtual network adapter used for ESXi management traffic (vMotion, IP storage, etc.).

**vMotion**
- Live migration of running VMs between ESXi hosts with no downtime.

**VMware Tools**
- Suite of utilities enhancing VM performance and management.

**VMX File**
- Virtual machine configuration file containing hardware and settings information.

**vNIC (Virtual Network Interface Card)**
- Virtual network adapter in a VM.

**vSAN (Virtual SAN)**
- VMware's software-defined storage solution.

**vSphere**
- VMware's virtualization platform (ESXi + vCenter Server).

**vSphere Client**
- Web-based interface for managing vCenter and ESXi (formerly called HTML5 Client).

**vSS (vSphere Standard Switch)**
- See Standard Switch.

## W

**WSFC (Windows Server Failover Clustering)**
- Microsoft clustering feature that can run on vSphere.

## X

**XVC vMotion**
- Cross-vCenter vMotion; migrating VMs between different vCenter Server instances.

---

## Acronyms

- **API** - Application Programming Interface
- **BIOS** - Basic Input/Output System
- **CPU** - Central Processing Unit
- **DAS** - Direct-Attached Storage
- **DCV** - Data Center Virtualization
- **DHCP** - Dynamic Host Configuration Protocol
- **DNS** - Domain Name System
- **DRS** - Distributed Resource Scheduler
- **ESXi** - Elastic Sky X Integrated
- **EVC** - Enhanced vMotion Compatibility
- **HA** - High Availability
- **HBA** - Host Bus Adapter
- **HCL** - Hardware Compatibility List
- **HTML** - Hypertext Markup Language
- **IP** - Internet Protocol
- **iSCSI** - Internet Small Computer Systems Interface
- **LAN** - Local Area Network
- **LUN** - Logical Unit Number
- **MAC** - Media Access Control
- **MPIO** - Multipath I/O
- **NAS** - Network-Attached Storage
- **NFC** - Network File Copy
- **NFS** - Network File System
- **NIC** - Network Interface Card
- **NUMA** - Non-Uniform Memory Access
- **OVA** - Open Virtual Appliance
- **OVF** - Open Virtualization Format
- **PSP** - Path Selection Policy
- **PSOD** - Purple Screen of Death
- **QoS** - Quality of Service
- **RAM** - Random Access Memory
- **RDM** - Raw Device Mapping
- **RPO** - Recovery Point Objective
- **RTO** - Recovery Time Objective
- **SAN** - Storage Area Network
- **SATP** - Storage Array Type Plugin
- **SCSI** - Small Computer System Interface
- **SDDC** - Software-Defined Data Center
- **SLA** - Service Level Agreement
- **SMP** - Symmetric Multiprocessing
- **SNMP** - Simple Network Management Protocol
- **SRM** - Site Recovery Manager
- **SSH** - Secure Shell
- **SSL** - Secure Sockets Layer
- **SSO** - Single Sign-On
- **STP** - Spanning Tree Protocol
- **SSD** - Solid State Drive
- **TCP** - Transmission Control Protocol
- **TPS** - Transparent Page Sharing
- **TSM** - Tech Support Mode
- **UEFI** - Unified Extensible Firmware Interface
- **UUID** - Universally Unique Identifier
- **vCLS** - vSphere Cluster Services
- **VCP** - VMware Certified Professional
- **vCPU** - Virtual CPU
- **VDS** - vSphere Distributed Switch
- **VLAN** - Virtual Local Area Network
- **VM** - Virtual Machine
- **VMDK** - Virtual Machine Disk
- **VMFS** - Virtual Machine File System
- **VMotion** - Virtual Motion
- **VMTN** - VMware Technology Network
- **VMX** - Virtual Machine Executable
- **vNIC** - Virtual Network Interface Card
- **VPN** - Virtual Private Network
- **vRAM** - Virtual RAM
- **vSAN** - Virtual SAN
- **vSphere** - Virtual Sphere
- **vSS** - vSphere Standard Switch
- **WAN** - Wide Area Network

---

**Note**: This glossary is regularly updated. For the most current definitions, consult VMware's official documentation.
