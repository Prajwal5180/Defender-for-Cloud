# Module 2 - Understanding your cloud attack surface
<br>
As you saw in Module 1, Defender for Cloud CSPM will help you identify weaknesses against best practices based on the workload running in your Azure Tenant / Subscription. These deviations are presented as recommendations and we performed a walkthrough of some of them. 

<br>

In this module we will how you can further extend this capability by generating your own queries to proactively hunt for points of entries to reduce the attack surface and decrease the likelihood of compromise.

## Contextualize cloud posture management

Defender for Cloud contains a graph-based context engine ***cloud security graph***.  The cloud security graph collects data from your multicloud environment and other data sources. For example, the cloud assets inventory, connections and lateral movement possibilities between resources, exposure to internet, permissions, network connections, vulnerabilities and more. The data collected is then used to build a graph representing your multicloud environment.

Defender for Cloud uses the graph to perform an attack path analysis (Attack Paths). You can also use the graph to find the issues with the highest risk that exist within your environment (cloud security explorer).

![Cloud Security Graph](../Images/mdfc-securitygraph.png?raw=true)

### Identify likely points of entry

1. Switch to ***Recommendations*** blade to see different Attack Paths that Defender has identified. Attack Path looks for points of entries and lateral movement not only in Azure, but also in AWS and GCP
![Attack Paths](../Images/mdfc-attackpath.png?raw=true)

2. Click on the Attack Path ***Internet exposed VM has high severity vulnerabilities and read permission to a Key Vault***
![Available Attack Paths](../Images/mdfc-attackpathsreco.png?raw=true)

3. Each attack path represents a scenario that you should be aware. The title itself provides you a quick understanding of how the risk exposure might manifest this allows you to quickly prioritize your investigation:
![Attack Paths example](../Images/mdfc-attackpathexample.png?raw=true)

4. To learn more about the particular Attack Path, simply select it. Here you can see that a publicy exposed VM that has a managed identity can read key vault. The path also gives you specifics of which VM and Key Vaults are potential targets.
![Attack Paths example scenario detail](../Images/mdfc-attackpathexampledetail.png?raw=true)

5. If you select the VM in the attack path, you will see the vulnerabilities and any security recommendations that are relevant to this machine. 
![Attack Paths VM detail](../Images/mdfc-attackpathvmedetail.png?raw=true)

6. If you select an ***Unhealthy*** recommendation, you will see the remediation steps and upon clicking the ***Take action*** button at bottom right of screen you will see the screen where you can implement these remediations.
![Attack Paths VM detail](../Images/mdfc-attackpathvmrecommendtiondetail.png?raw=true)

7. Now you have a complete picture of:
   - What resources can cause potential risk exposure
   - What is a likely path that leads to exposure
   - What are the open recommendations on these resources
   - How to remediate open attack paths

### Building and exploring your own custom risk scenarios

1. Select the ***Cloud Security Explorer*** blade. You will see an option to build your own no-code query and a some sample starter templates. We will model our own scenaio here.
   ![Cloud Security Explorer](../Images/mdfc-cloudsecurityexplorer.png?raw=true)

2. Let's build our scenario where we will identify public vulnerable machines that can access object storage
3. Choose *Internet exposed VMs with high severity vulnerabilities* template from **Query Templates** and click Search
   ![Cloud Security Explorer VM example](../Images/mdfc-cloudsecurityexplorerexample.png?raw=true)
4. You will see a list of machines that are not only publicly exposed but also are vulnerable. Now, let's expand this to identify machines that have permissions to other resources (managed identities). 
5. Click on the plus next to Virtual Machines (group)![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexplorerplus.png?raw=true)
6. Select Identity & Access > Can authenticate as ![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexploreridentity.png?raw=true)
7. Select Application Identities and click Done ![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexplorerappidentity.png?raw=true)
8. Now let's add the resource type to which this VM has access via managed identity. Select the + sign next to Application identities(group), select Identity & Access and Has permissions to ![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexplorermiaccess.png?raw=true)
9. Now you will need to select the type of resource that this VM can access using a managed identity ![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexplorermiaccess2.png?raw=true)
10. Click on the + sign next to Type of Resource and you will see the resource types you can query. We will select Object Storage and select Done. ![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexplorermiaccess3.png?raw=true). 
11. When we click search you will see a list of machines that can be the target of this attack path ![Cloud Security Explorer Custom Scenario](../Images/mdfc-cloudsecurityexplorersearchresults.png?raw=true). 

### Continue with the next module: [Module 3 - Dashboards](../Modules/Module3:Dashboards.md)
