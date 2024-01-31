Q1, Interesting question on cost management where multiple subscriptions was not the right answer

Q8,  IoT Hub

Q11,  3TB to 4TB db, replicas; Azure SQL Versions
  - AzSQL at P6 only supports 500 GB, need P11 pr P15 to get the storage and does not support replicas
  - hyperscale supports 4 r/o replicas, expensive but satisfies requirements
  - SQL Managed, vCore, Business Critical service tier. up to 4TB and multi r/o replicas

Q14, Azure VM availability set in active/passive mode

Q17, migrate to Azure
  - migrate 35G from NAS to Azure
  - AzCopy for GB level migration
  - File Sync good for File Shares
  - Data Box good for up to 100TB

Q22,
  - microservice architecture allows customization of the OS and resource allocation

Q26:
  - P2S VPN and S2S VPN
  - Express Route is for WAN, not for remote worker VPN

Q30: Container Insights for AKS (part of Azure Monitor)
  - Azure Monitor
  - https://learn.microsoft.com/en-us/azure/azure-monitor/containers/container-insights-overview
  - https://learn.microsoft.com/en-us/azure/azure-monitor/vm/vminsights-overview
  - https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/grafana-plugin

Q34: SSO scenario, SSO with password hash syncy
 - https://learn.microsoft.com/en-us/entra/identity/hybrid/connect/choose-ad-authn
 - pass-through auth requires an agent

Q35: conditional access policy for MFA by department
 - https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-methods

Q36: https://learn.microsoft.com/en-us/azure/security/fundamentals/steps-secure-identity

Q37: AD auth with no passwords in the cloud
 - https://learn.microsoft.com/en-us/entra/identity/hybrid/connect/choose-ad-authn

Q38: 

Q45: automatic user removal
 - Access reviews can automatically review users after a review period
 - Expiration policies apply to M365 groups, not security groups

Q46: AAD P2 Identity Protection

Q48: Azure Key Vault to protect secrets vs. Managed Identity/service principals which is more work

Q52: Key vault tags, keys, secrets and certs

Q54: Continous Access Evaluation (CAE)
 - https://learn.microsoft.com/en-us/entra/identity/conditional-access/concept-continuous-access-evaluation

Q56: Azure Policy minimum required. Multiple conditions in one policy and use AllOf operator.
 -  https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-setup-guide/organize-resources?tabs=AzureManagementGroupsAndHierarchy
 - https://learn.microsoft.com/en-us/azure/governance/policy/concepts/definition-structure

Q60: Resource tags can be applied to a subscription

Q61: https://learn.microsoft.com/en-us/azure/governance/blueprints/concepts/lifecycle

Q62: Azure Blueprints https://learn.microsoft.com/en-us/azure/governance/blueprints/overview

Q65: Access Package part of Entitlement Management
 - https://learn.microsoft.com/en-us/entra/id-governance/entitlement-management-access-package-first
 - lifecycle workflows: https://learn.microsoft.com/en-us/entra/id-governance/what-are-lifecycle-workflows
 - access reviews: https://learn.microsoft.com/en-us/entra/id-governance/entitlement-management-access-package-first

Q69: Azure SQL Transparent Data Encryption
 - encrypt data at rest
 - Always Encrypt includes in transit and requires additiona effort https://learn.microsoft.com/en-us/sql/relational-databases/security/encryption/always-encrypted-tutorial-getting-started?view=sql-server-ver16&tabs=ssms

 Q70: Azure SQL Configuration
  - Premium tier for in memory OLTP and columnstore indexes
  - Standard tier non critical production
  - 1000 DTUs up to 10 GB in memory OLTP
  - 500 DTUs up to 4 GB im memory OLTP
  - 125 DTUs up to 1 GB in memory OLTP
  - https://learn.microsoft.com/en-us/azure/azure-sql/database/resource-limits-dtu-elastic-pools?view=azuresql
  - https://learn.microsoft.com/en-us/azure/azure-sql/database/service-tiers-dtu?view=azuresql

Q72: Azure SQL Managed Instance and Always Encrypted
 - identify sensitive data and protect from admin and db_owner et.al.
 - https://learn.microsoft.com/en-us/azure/azure-sql/database/service-tiers-dtu?view=azuresql
 - security capabilities https://learn.microsoft.com/en-us/azure/azure-sql/database/security-overview?view=azuresql

Q73: Azure SQL vs. MI 
 - Managed Instance does not support DTU pricing model
 - Azure SQL can support up to 100TB, Managed Instance is only 4 TB
 - https://learn.microsoft.com/en-us/azure/azure-sql/database/elastic-pool-overview?view=azuresql-db

Q79: Strorage access tiers
 - can be set on individual block blobs

Q83: Azure Data Factory incremental copy
 - Azure Data Migration Assistant is for SQL Server
 - https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-migrate-gen1-to-gen2


Q90: https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview

Q91: service SAS https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview

Q93: Stream Analytics and Event Hubs for sending messages
 - https://learn.microsoft.com/en-us/azure/event-hubs/event-hubs-about
 - https://learn.microsoft.com/en-us/azure/stream-analytics/stream-analytics-add-inputs

Q95: Cool access tier
 - 99% availability
 - millisecond responsde
 - low cost storage when infrequent access

Q97: storage redundancy configuration and options
 - GRS and GZRS are for the secondary region, not the primary
 - GRS equates to LRS and GZRS goes with ZRS
 - Zone redundant: multiple data centers within a region
 - https://learn.microsoft.com/en-us/training/modules/design-data-storage-solution-for-non-relational-data/4-design-for-data-redundancy
 - RA (Read Access) must be configured if desired

Q99: Azure SQL DR with RTO nte 30 secons and RPO nte 5 seconds
 - auto geo failover waits one hour to trigger to prevent premature failover
 - geo restores based on geo-redundant backups have 1 hour RPO and 12 hour RTO
 - https://learn.microsoft.com/en-us/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview?view=azuresql

Q100: Azure encryption key option
 - can be applied to all types, but, must be configured at account creation time
 - https://learn.microsoft.com/en-us/azure/security/fundamentals/encryption-overview

Q101: SQL Server on a VM
 - https://learn.microsoft.com/en-us/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices-checklist?view=azuresql
 - local storage for TempDB

Q102: ADF Self hosted runtimes

Q103: Azure Databricks for ML and query Delta Live Tables using Databricks SQL
 - https://learn.microsoft.com/en-us/azure/databricks/introduction/
 - https://learn.microsoft.com/en-us/azure/databricks/delta-live-tables/publish

Q104: Azure Synapse Analytics and Apache Spark
 - Review Azure Synapse Analytics
 - built in
 - "private link"

Q105: Azure SQL Hyperscale
 - Hyperscale tier required to get to 100TB (the max)
 - https://learn.microsoft.com/en-us/azure/azure-sql/database/service-tier-hyperscale-frequently-asked-questions-faq?view=azuresql
 - https://learn.microsoft.com/en-us/azure/azure-sql/database/single-database-overview?view=azuresql

 - Azure SQL Deployment models, Single database, elastic pool

Q106: Azure Stream Analytics functions
 - Windowing, Aggregate, Date/Time, Array
 - https://learn.microsoft.com/en-us/stream-analytics-query/windowing-azure-stream-analytics

Q107: Azure Synapse Analytics
 - remember this is a version of SQL Server
 - materialized views to cache data/optimize queries
 - Synaps workspace includes a Serverless Pool
 - result set caching designed for relatively static data

https://learn.microsoft.com/en-us/training/modules/design-data-integration/5-solution-azure-synapse-analytics

https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-a-data-lake/

Q110: Azure Site Recovery
 - cache storage accounts get created in source region
 - VM writes are written to cache storage wcich is then replicated to target region
 - https://learn.microsoft.com/en-us/azure/site-recovery/azure-to-azure-tutorial-enable-replication

Q112: SQL Backup retention options
 - LTR up to 10 years can be configured for Azure SQL and Azure Managed SQL
 - 

Q113: minimum RPO
 - GRS: v1, v2, blob storage accounts
 - SQL Server Availability Groups
 - log shipping requires manual failback
 - Azure Site Recovery for VMs

Q114: AKS configuration
 - multiple clusters in paired regions delays updates in the pair to reduce impact of updates
 - nodepool deployed in availablity sets helps with datacenter failurs in a region
 - geo replication reduce network egress
 - Traffic Manager vs. App Gateway vs Load Balancer
  https://learn.microsoft.com/en-us/azure/container-registry/container-registry-geo-replication
  https://learn.microsoft.com/en-us/azure/aks/operator-best-practices-multi-region

Q117: review business continuity with SQL
 - https://learn.microsoft.com/en-us/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview?view=azuresql

Q118: data protection https://learn.microsoft.com/en-us/azure/storage/blobs/data-protection-overview

Q120: https://learn.microsoft.com/en-us/azure/architecture/guide/design-principles/redundancy

Q121: high scalability website
 - web app limited to 50 instances
 - VMSS can scal to 1000
 - Availability sets are legacy, use VMSS instaed
   - different fault domains
   - reduce vm to vm latency
 - availability zones

Q125: Azure Traffic Manager vs. Azure Load Balancer

Q136: Azure Monitor config
 - https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/diagnostic-settings

Q127: Traffic Manager 6 routing methods 
 - https://learn.microsoft.com/en-us/azure/traffic-manager/traffic-manager-routing-methods
 - priority configure which endpoints have priority
 - weitghted does not differentiate region
 - multivalue: query endpoints and level load

Q128: Azure Cosmos DB consistency

Q129: VM sizing 
 - https://learn.microsoft.com/en-us/azure/virtual-machines/sizes

Q131: VM sizing
 - F series has higher CPU to memory ratio
 - E series is for heavy in-memory operations ex SAP Hana
 - Dv3 intended for realation db. Optimal CPU to memory config. Can run most production workloads

Q141: Azure Service Bus topics
 - multiple receivers
 - subscribe to topic
 - poll a queue
 
Q145: Packer and Terraform
- deploy VM with a custom image
- use existing Ansible playbooks
- is Terraform on the exam?

Q149: According to the questions, an existing on premise web service can be migrated to Azure App Service with no changes. This is probabably true?

Q150: Azure Migrate
- https://learn.microsoft.com/en-us/azure/migrate/migrate-services-overview
- https://learn.microsoft.com/en-us/azure/migrate/resources-faq
- https://learn.microsoft.com/en-us/azure/migrate/concepts-migration-planning
- Includes SQL Migration but no non-relational tooling
- web apps and VMs

Q151: Azure Migrate 
- can migrate "live": replicates and syncs to prep for switchover

Q152: Azure AD vs. AD

Q154: Microsoft Cloud Adoption Framework
- https://learn.microsoft.com/en-us/training/modules/design-migrations/2-evaluate-migration-cloud-adoption-framework

Q157: ASGs and NSGs
- https://learn.microsoft.com/en-us/azure/virtual-network/application-security-groups
- https://learn.microsoft.com/en-us/azure/virtual-network/network-security-groups-overview

Q158: standard Load Balancer and SQL Server availability group
- https://learn.microsoft.com/en-us/azure/azure-sql/virtual-machines/windows/availability-group-load-balancer-portal-configure?view=azuresql
- https://learn.microsoft.com/en-us/azure/networking/fundamentals/networking-overview

Q162: App Gateway vs. Load Balancer
- "gateway" vs. simple load balancing
- https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/load-balancing-overview

Q166: Routing decisions means L7 and App Gateway
- https://learn.microsoft.com/en-us/azure/application-gateway/overview

Q167: Secure high bandwidth connection to on prem from vnet
- Express Route and Private Link
- Private link connects to servcie (express route) via a private connection

