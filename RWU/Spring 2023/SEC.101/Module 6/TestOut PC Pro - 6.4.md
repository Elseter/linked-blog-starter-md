
---
aliases: [ "20230223125432",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-23 12:54
---
[[SEC.101 Index]]
# TestOut PC Pro - 6.4
---
## 6.4.2 Virtualization Facts
- This less on convers the following topics
	- Purpose of Virtualization
	- Virtualization Components

### Purpose of Virtualization
Virtualization is a technology that creates a software-based representation of component, such as an application, network interface card (NIC), or even an entire computer. On a computer system, virtualization is the ability to install and run multiple operating systems simultaneously on a single physical machine. These types of systems are commonly referred to as VMs (virtual machines).

#### Benefits of Virtualization
##### Sandbox Virtualization
The process of creating an isolated testing environment. Virtualization lets you easily create a sandbox by isolating components from the production network.  
  
Using a virtualized sandbox (sometimes known as a playground) gives network administrators and developers a safe place to create new software, test software development, install new software, or upgrade existing software without risking the production network.

##### Application Virtualization
The process of installing and accessing applications virtually. This can help reduce licensing costs; increase accessibility for local and remote employees; and make it easier to install and maintain applications.

##### Legacy Software Access
Outdated software use. Some organizations require the use of proprietary or legacy (outdated) software. Virtualization can provide access to this software even if a user’s local PC is running an updated operating system.

##### Cross-Platform Virtualization
The process allowing an operating system to access an application designed to run on a different operating system.

##### Hardware Optimization
The process of making the most efficient use of physical hardware. For example, instead of being idle, the processor is optimized to process several tasks at a time.

### Virtualization Components
#### Components
##### Host Machine
Most commonly a physical server that has the hardware necessary to create a viable, virtualized environment. The following hardware is shared by the VM and managed by the hypervisor.

-   Hard disk drive(s)
-   Optical drive(s)
-   RAM
-   CPU(s)
-   NIC(s)
The number of VMs a host can handle depends on the physical build of the host server.

##### Hypervisor
A thin layer of software (think of it as a type of OS for the host machine) that resides between the virtual operating system and the hardware. A hypervisor allows virtual machines to interact with the hardware without going through the host operating system.

##### Virtual Machine
A software implementation of a computer that executes programs like a physical machine. The virtual machine appears to be a self-contained and autonomous system. It can be on a host server (enterprise-level) or a PC (small scale).

##### Virtual hard disk (VHD)
A file created within the host operating system that simulates a hard disk for the virtual machine.

##### vSwitch
Software that facilitates the communication between virtual machines by checking data packets before moving them to a destination. A vSwitch may be software installed on the virtual machine or it may be part of the server firmware.

##### vRouter
Software that performs the tasks of a physical router. Because virtual routing frees the IP routing function from specific hardware, you can move routing functions around a network.

##### Virtual firewall application (VFA)
Software that functions as a network firewall device that provides packet filtering and monitoring. The VFA can run as a traditional software firewall on a virtual machine.

## 6.4.5 Hyper-V Facts
- This lesson covers
	- Hyper-V
	- Hyper-V in Windows 11

### Hyper-V
A hypervisor is a thin layer of software (think of it as a type of OS for the host machine) that resides between the virtual operating system and the hardware. A hypervisor allows virtual machines to interact with the hardware without going through the host operating system.

#### Characteristics
##### Type
There are two types of hypervisors:
-   Type 1 - Also called bare metal, acts as an OS on a physical host machine.
-   Type 2 - Acts as a software application. It is run on any OS and can run several operating systems on virtual machines. Capacity is limited by available physical assets.

##### Number of VMs supported
The number of VMs a host can accommodate depends on the components installed on the host machine and what has already been allocated by the Hyper-V manager. Keep in mind:

-   Close to 80% of all VMs are over-provisioned. This means they have more resources allocated to them than is needed.
-   This decreases the efficacy of the physical host.
-   When provisioning, consider:
    -   CPU and RAM allocations can be lowered or raised easily.
    -   Storage space can be easily increased but is almost impossible to decrease without destroying the VM.

##### System resource access
A hypervisor manages access to the following system resources.
-   CPU
-   Storage
-   RAM

##### Hypervisor options
There are several hypervisor options:
-   Hyper-V (Windows)
-   VMWare workstation
-   Virtual Box (Oracle)

### Hyper-V in Windows 11
#### How to Use
##### Enable Hyper-V
1.  Access Control Panel and select **Programs**.
2.  Under Programs and Features, select **Turn Windows features on or off**.
3.  Expand **Hyper-V**.
4.  Place checkmarks by **Hyper-V Management Tools** and **Hyper-V Platform**. (If Hyper-V Platform is grayed out, virtualization support has been disabled in the firmware. Refer to the BIOS/firmware documentation for instructions to enable.  
    ![UI for adding Hyper-V](https://cdn.testout.com/_version_7030/pcpro2022v7-en-us/en-us/resources/text/t_win_virt_pp7/hyper-v.jpg)
##### Configure virtual networking
To configure virtual networking:
-   Choose the type of network you want to set up (external, internal, or private).
-   Use the Virtual Switch Manager to select a NIC if you are configuring an external virtual network

##### Create Virtual Machine
To create virtual machines, run Hyper-V Manager and specify the following parameters:
-   A name for the new VM.
-   The virtual machine's generation.
-   The amount of RAM the VM is allowed to use.
-   The shared network switch that you created earlier for the VM to use for networking.
-   The VHD file you want to use. You can create a new VHD file or use an existing one.
-   The optical drive or ISO file you want to use to access the operating system files.

##### Start the virtual machine
To start the virtual machine, power it on in Hyper-V Manager. If you created a new VHD file, you must install an operating system.  
  
If you choose to install Windows, you should install Integration Services (IS) after the installation is complete. IS:

-   Dramatically improves VM performance by installing (in the VM) modified disk, network, and mouse drivers that are Hyper-V aware.
-   Lets you cut and paste between the host and guest Windows operating systems installed within VMs.
-   Enables the mouse to move smoothly in and out of the Virtual Machine Connection window.

##### Move the virtual machine
You use the Virtual Machine Connection window to interact with a VM. To connect to a VM, run Hyper-V Manager, select the VM that you want to access, and connect to it. You can start, stop, pause, and take snapshots (also called checkpoints) of the virtual machine's current configuration using the Hyper-V Manager window.