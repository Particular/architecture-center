---
title: Scenarios that feature Microsoft on-premises technologies on Azure
description: Review a list of architectures and solutions that use Microsoft on-premises technologies on Microsoft Azure.
author: martinekuan
ms.author: pnp
ms.date: 07/26/2022
ms.topic: conceptual
ms.service: azure-architecture-center
ms.subservice: architecture-guide
products:
  - windows-server
  - office-exchange-server
  - sql-server
  - entra-id
  - azure-virtual-machines-windows
categories:
  - mobile
  - hybrid
  - identity
  - azure-virtual-desktop
  - web
  - networking
  - management-and-governance
  - devops
  - databases
  - integration 
  - analytics
  - storage
ms.custom: fcp
---

# Scenarios featuring Microsoft on-premises technologies on Azure

This article describes scenarios that feature Microsoft on-premises technologies on Azure. These scenarios enable you to gain the benefits provided by the cloud when you use technologies that were historically used in a local environment. The following on-premises technologies are frequently used in Azure solutions: 
- [Windows Server 2022](https://www.microsoft.com/windows-server). The foundation of the Microsoft ecosystem. It continues to power the hybrid cloud network.
- [SQL Server 2019](https://www.microsoft.com/sql-server/sql-server-2019). The data platform that's known for performance, security, and availability.
- [Exchange Server](/exchange/new-features/new-features). The messaging platform that provides email, scheduling, and tools for custom collaboration and messaging service applications.
- [Active Directory Domain Services in Windows Server 2016](/windows-server/identity/whats-new-active-directory-domain-services). The service that stores information about user accounts and enables other authorized users on the same network to access it. Security is integrated with Active Directory through sign-in authentication and access control to objects in the directory.
- [Host Integration Server](/host-integration-server/what-is-his). Technologies and tools that enable enterprise organizations to integrate existing IBM host systems, programs, messages, and data with new Microsoft server applications. 

For information about solutions in which Azure services integrate with the other Microsoft cloud platforms, see these articles:
- [Azure and Power Platform scenarios](../solutions/power-platform-scenarios.md)
- [Azure and Microsoft 365 scenarios](../solutions/microsoft-365-scenarios.md)

## Active Directory

|Architecture|Summary|Technology focus|
|--|--|--|
|[Azure files secured by AD DS](../example-scenario/hybrid/azure-files-on-premises-authentication.yml)|Provide high-security file access with on-premises Windows Server Active Directory Domain Services (AD DS) and DNS.| Hybrid|
|[Create an AD DS resource forest](../reference-architectures/identity/adds-forest.yml)|Learn how to create a separate Active Directory domain on Azure that's trusted by domains in your on-premises Active Directory forest.| Identity|
|[Deploy AD DS in an Azure virtual network](../reference-architectures/identity/adds-extend-domain.yml)|Use this reference architecture to extend an on-premises Active Directory domain to Azure to provide distributed authentication services.| Identity|
|[Enable VM protection in Azure Site Recovery](/azure-stack/operator/protect-virtual-machines) |Learn about an optimized approach to disaster recovery of VM-based user workloads that are hosted on Azure Stack Hub. Azure Site Recovery integrates with Windows Server-based apps and roles, including Active Directory Domain Services.|Hybrid|
|[Extend on-premises AD FS to Azure](../reference-architectures/identity/adfs.yml) |Implement a highly secure hybrid network architecture by using Active Directory Federation Services (AD FS) authorization on Azure.|Identity|
|[Multiple forests with AD DS and Microsoft Entra ID](../example-scenario/azure-virtual-desktop/multi-forest.yml)|Create multiple Active Directory forests by using Azure Virtual Desktop.|Virtual Desktop|
|[On-premises Active Directory domains with Microsoft Entra ID](../reference-architectures/identity/azure-ad.yml) |Learn how to implement a secure hybrid network architecture that integrates on-premises Active Directory domains with Microsoft Entra ID.|Identity|
|[Use Azure file shares in a hybrid environment](../hybrid/azure-file-share.yml) |Use identity-based authentication to control access to Azure file shares via AD DS users and groups.|Hybrid|

## Exchange Server

|Architecture|Summary|Technology focus|
|--|--|--|
|[Back up files and apps on Azure Stack Hub](/azure/backup/backup-mabs-files-applications-azure-stack)|Learn about an optimized approach to backing up and restoring files and applications of VM-based user workloads that are hosted on Azure Stack Hub. Includes backup and restore of Exchange Server servers and databases.| Hybrid|
|[Enable VM protection in Azure Site Recovery](/azure-stack/operator/protect-virtual-machines) |Learn about an optimized approach to disaster recovery of VM-based user workloads that are hosted on Azure Stack Hub. Includes a discussion of disaster recovery for Exchange workloads.|Hybrid|
|[Enhanced-security hybrid messaging - client access](../example-scenario/hybrid/secure-hybrid-messaging-client.yml)|Enhance your security in a client access scenario by using Microsoft Entra multifactor authentication. Discusses scenarios for Exchange Online and Exchange on-premises.| Hybrid|
|[Enhanced-security hybrid messaging - mobile access](../example-scenario/hybrid/secure-hybrid-messaging-mobile.yml)|Enhance your security in a mobile access scenario by using Microsoft Entra multifactor authentication. Discusses scenarios for Exchange Online and Exchange on-premises.|Hybrid|
|[Enhanced-security hybrid messaging - web access](../example-scenario/hybrid/secure-hybrid-messaging-web.yml) |Enhance your security in a web access scenario by using Microsoft Entra multifactor authentication. Discusses scenarios for Exchange Online and Exchange on-premises.|Hybrid|

## Host Integration Server (HIS)

|Architecture|Summary|Technology focus|
|--|--|--|
|[Integrate IBM mainframe and midrange message queues with Azure](../example-scenario/mainframe/integrate-ibm-message-queues-azure.yml) |Learn about a data-first approach to middleware integration that enables IBM message queues. HIS is used in a VM-based IaaS approach.|Mainframe|
|[Mainframe file replication and sync on Azure](../solution-ideas/articles/mainframe-azure-file-replication.yml) |Learn several options for moving, converting, transforming, and storing mainframe and midrange file system data on-premises and on Azure. HIS is used to convert EBCDIC files to make them compatible with Azure.|Mainframe|

## SharePoint Server

|Architecture|Summary|Technology focus|
|--|--|--|
|[Back up files and apps on Azure Stack Hub](/azure/backup/backup-mabs-files-applications-azure-stack)|Learn about an optimized approach to backing up and restoring files and applications of VM-based user workloads that are hosted on Azure Stack Hub. Includes backup and restore of SharePoint farms and front-end web server content and restore of SharePoint databases, web apps, files, list items, and search components.|Hybrid|
|[Enable VM protection in Azure Site Recovery](/azure-stack/operator/protect-virtual-machines)|Learn about an optimized approach to disaster recovery of VM-based user workloads that are hosted on Azure Stack Hub. Includes information about disaster recovery for SharePoint workloads.| Hybrid|
|[Highly available SharePoint farm](../solution-ideas/articles/highly-available-sharepoint-farm.yml) |Deploy a highly available SharePoint farm for intranet capabilities that uses Microsoft Entra ID, a SQL Server Always On instance, and SharePoint resources.|Web|
|[Multitier web application built for HA/DR](../example-scenario/infrastructure/multi-tier-app-disaster-recovery.yml) |Learn how to create a resilient multitier web application that's built for high availability and disaster recovery on Azure. Applies to applications like SharePoint.|Networking|

## SQL Server

|Architecture|Summary|Technology focus|
|--|--|--|
|[Back up files and apps on Azure Stack Hub](/azure/backup/backup-mabs-files-applications-azure-stack) |Learn about an optimized approach to backing up and restoring files and applications of VM-based user workloads that are hosted on Azure Stack Hub. Includes backup and restore of SQL Server instances and their databases.|Hybrid|
|[Enable VM protection in Azure Site Recovery](/azure-stack/operator/protect-virtual-machines) |Learn about an optimized approach to disaster recovery of VM-based user workloads that are hosted on Azure Stack Hub. Includes information about disaster recovery for SQL Server workloads.|Hybrid|
|[Enterprise business intelligence](/azure/architecture/example-scenario/analytics/enterprise-bi-synapse) |Learn how to implement an ELT pipeline that moves data from an on-premises SQL Server database into Azure Synapse Analytics and transforms the data for analysis.|Integration|
|[Mainframe access to Azure databases](../solution-ideas/articles/mainframe-access-azure-databases.yml) |Give mainframe applications access to Azure data without changing code. Use Microsoft Service for DRDA to run Db2 SQL statements on a SQL Server database.|Mainframe|
|[Micro Focus Enterprise Server on Azure VMs](../example-scenario/mainframe/micro-focus-server.yml)|Optimize, modernize, and streamline IBM z/OS mainframe applications by using Micro Focus Enterprise Server 6.0 on Azure VMs. This solution uses a SQL Server IaaS database in an Always On cluster.| Mainframe|
|[Optimize administration of SQL Server instances in on-premises and multicloud environments by using Azure Arc](../hybrid/azure-arc-sql-server.yml) |Learn how to use Azure Arc for the management, maintenance, and monitoring of SQL Server instances in on-premises and multicloud environments.|Databases|
|[Plan deployment for updating Windows VMs on Azure](../example-scenario/wsus/index.yml)|Learn best practices for configuring your environment for Windows Server Update Services (WSUS). SQL Server is the recommended database for servers that support a high number of client computers.|Management|
|[SQL Server 2008 R2 failover cluster on Azure](../example-scenario/sql-failover/sql-failover-2008r2.yml) |Learn how to rehost SQL Server 2008 R2 failover clusters on Azure virtual machines. |Databases|
|[SQL Server on Azure Virtual Machines with Azure NetApp Files](../example-scenario/file-storage/sql-server-azure-netapp-files.yml) |Implement a high-bandwidth, low-latency solution for SQL Server workloads. Use Azure NetApp Files for enterprise-scale performance and reduced costs.|Storage|
|[Web app private connectivity to Azure SQL Database](../example-scenario/private-web-app/private-web-app.yml) |Lock down access to an Azure SQL database with Azure Private Link connectivity from a multitenant web app.|Web|

[Browse all our SQL Server solutions](/azure/architecture/browse/?products=sql-server).

## Windows Server

|Architecture|Summary|Technology focus|
|--|--|--|
|[Azure files secured by AD DS](../example-scenario/hybrid/azure-files-on-premises-authentication.yml) |Provide high-security file access with on-premises Windows Server AD DS and DNS.|Hybrid|
|[Back up files and apps on Azure Stack Hub](/azure/backup/backup-mabs-files-applications-azure-stack) |Learn about an optimized approach to backing up and restoring files and applications of VM-based user workloads that are hosted on Azure Stack Hub. Supports backup and restore of various resources on VMs that run Windows Server. |Hybrid|
|[Enable VM protection in Azure Site Recovery](/azure-stack/operator/protect-virtual-machines) |Learn about an optimized approach to disaster recovery of VM-based user workloads that are hosted on Azure Stack Hub. Includes information about providing disaster recovery for Azure Stack Hub VMs that run Windows Server operating systems.|Hybrid|
|[Plan deployment for updating Windows VMs on Azure](../example-scenario/wsus/index.yml)|Learn best practices for configuring your environment for WSUS.|Management|
|[Run SAP NetWeaver in Windows on Azure](/azure/architecture/guide/sap/sap-netweaver)|Learn proven practices for running SAP NetWeaver in a Windows environment on Azure.|SAP|
|[SQL Server 2008 R2 failover cluster on Azure](../example-scenario/sql-failover/sql-failover-2008r2.yml) |Learn how to rehost SQL Server 2008 R2 failover clusters on Azure virtual machines. Use the Azure shared disks feature and a Windows Server 2008 R2 failover cluster to replicate your on-premises deployment on Azure.|Databases|

## Related resources

- [Microsoft partner and third-party scenarios on Azure](partner-scenarios.md)
- [Architecture for startups](../guide/startups/startup-architecture.md)
- [Azure and Power Platform scenarios](../solutions/power-platform-scenarios.md)
- [Azure and Microsoft 365 scenarios](../solutions/microsoft-365-scenarios.md)
- [Azure and Dynamics 365 scenarios](../solutions/dynamics-365-scenarios.md)
- [Azure for AWS professionals](../aws-professional/index.md)
- [Azure for Google Cloud professionals](../gcp-professional/index.md)
