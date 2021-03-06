# Dashboards

LogicMonitor dashboards, provisioned with all new LogicMonitor accounts. When importing to an existing account, change the value of the ##defaultResourceGroup## or ##defaultResourceName## token to select the relevant group of devices (or individual device) for which you wish to visualize data. Intended to be examples to get the creativity flowing! (LogicMonitor Support can always help with adjustments)

These dashboards depend on the presence of the latest versions of LogicMonitor datasources, and dynamic groups in the 'Devices by Type' device group. If these groups don't exist, they can be created using the out-of-box PropertySources from LogicMonitor together with the below documentation. [So make sure you have the latest PropertySources (and DataSources) from the repository!](https://www.logicmonitor.com/support/settings/logicmodules/keeping-your-datasources-up-to-date/)

To see a preview of what some of these dashboards look like, visit the [LogicMonitor Dashboard Gallery](https://www.logicmonitor.com/sales/dashboards/).

To download all dashboards as a single file, see [LogicMonitor Dashboards](https://github.com/kdevilbiss/Dashboards/blob/master/Dashboard%20Groups/LogicMonitor%20Dashboards.json) in the [Dashboard Groups](https://github.com/kdevilbiss/Dashboards/tree/master/Dashboard%20Groups) directory.

**LogicMonitor Default Dashboards** 

Format: Dashboard Name | Required Dynamic Group Name | Dynamic Group Definition

**Alerting**
- Alert List | * | (No specific group requirement)
- Alert Overview | * | (No specific group requirement)
- Geo_Alert_Map | * | (No specific group requirement)
- SLA_Overview | * | (No specific group requirement)

**Applications**
- Apache | Devices by Type/ Linux Servers | isLinux()
- Citrix XenApp / XenDesktop | * | (No specific group requirement)
- Docker | Devices by Type/ Linux Servers | isLinux()
- Nginx | Devices by Type/ Linux Servers | isLinux()
- Office 365 | * | (No specific group requirement)
- Zoom | * | (No specific group requirement)

**Databases**
- SQL Server | Devices by Type/ SQL Servers | hasCategory("MSSQL")

**Hardware**
- APC | * | (No specific group requirement)
- Dell iDRAC | * | (No specific group requirement)
- HP iLO | * | (No specific group requirement)

**Kubernetes**
- Kubernetes Cluster Overview | * | (No specific group requirement)
- k8s Cluster | * | (No specific group requirement)
- k8s Pods | * | (No specific group requirement)

**Linux**
- Linux | Devices by Type/ Linux Servers | isLinux()
- Linux (SSH) | Devices by Type/ Linux Servers | isLinux()

**LogicMonitor**
- Collectors | Devices by Type/ Collectors | hasCategory("Collectors")
- LogicMonitor Portal Metrics | * | (Requires the LogicMonitor Portal Metrics datasource)
- Resource Utilization | * | (No specific group requirement)
- Welcome to LogicMonitor | * | (No specific group requirement)

**Microsoft**
- Active Directory | Devices by Type/ Windows Servers | isWindows()
- DHCP Servers | Devices by Type/ Windows Servers | isWindows()
- DNS Servers | Devices by Type/ Windows Servers | isWindows()
- File Servers | Devices by Type/ Windows Servers | isWindows()
- Windows | Devices by Type/ Windows Servers | isWindows()

**Network**

- Cisco ASA | * | (No specific group requirement)
- Cisco Wireless | Devices by Type/ Network | (No specific group requirement)
- Local Network Latency | Devices by Type/* | (No specific group requirement)
- Network Performance | Devices by Type/ Network | isNetwork()
- Palo Alto | Devices by Type/ Palo Alto | hasCategory("PaloAlto")
- Ubiquiti Unifi | Devices by Type/ Network | isNetwork()

**Storage**
- NetApp | * | (No specific group requirement)

**Virtualization**
- Cisco Hyperflex | * | (No specific group requirement)
- Hyper-V | Devices by Type/ Hyper-V | hasCategory("HyperV")
- Nutanix | * | (No specific group requirement)
- vSphere_ESXi_Overview | Devices by Type/ VMware Hosts | system.virtualization =~ "VMware ESXi Host"
- vSphere_vCenter_Overview | Devices by Type/ VMware vCenters | system.virtualization =~ "VMware ESXi vCenter"
