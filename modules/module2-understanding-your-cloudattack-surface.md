# Module 2 - Understanding your cloud attack surface
<br>
As you saw in Module 1, Defender for Cloud CSPM will help you identify weaknesses against best practices based on the workload running in your Azure Tenant / Subscription. These deviations are presented as recommendations and we performed a walkthrough of some of them. 

<br>

In this module, we will how you can further extend this capability by generating your own queries to proactively hunt for points of entries to reduce the attack surface and decrease the likelihood of compromise.

## Contextualize cloud posture management

Defender for Cloud contains a graph-based context engine ***cloud security graph***.  The cloud security graph collects data from your multi-cloud environment and other data sources. For example, the cloud assets inventory, connections and lateral movement possibilities between resources, exposure to the internet, permissions, network connections, vulnerabilities, and more. The data collected is then used to build a graph representing your multi-cloud environment.

Defender for Cloud uses the graph to perform an attack path analysis (Attack Paths). You can also use the graph to find the issues with the highest risk that exist within your environment (cloud security explorer).

![Cloud Security Graph](../images/mdfc-securitygraph1.png)

### Task 1: Identify likely points of entry

1. In Azure Portal, search for **Microsoft Defender for Cloud (1)** and then click on it from the search results (2).

   ![Attack Paths](../images/M0-T1-S1.1.png)

2. From **Defender for Cloud** menu, click on the **Recommendations (1)** blade to see different Attack Paths that Defender has identified. Attack Path looks for points of entries and lateral movement not only in Azure but also in AWS and GCP. Click on the **Attack path (2)**.

   ![Attack Paths](../images/mdfc-attackpath.png?raw=true)

3. In **Microsoft Defender for Cloud | Attack path analysis** page. Each attack path represents a scenario that you should be aware of. The title **Internet exposed VM has high severity vulnerabilities and read permission to a Key Vault (1)** itself provides you a quick understanding of how the risk exposure might manifest, this allows you to quickly prioritize your investigation.

   ![Attack Paths example](../images/mdfc-attackpathexample1.png?raw=true)

5. Select **Internet exposed VM has high severity vulnerabilities and read permission to a Key Vault (1)** under Attack path.

   ![Available Attack Paths](../images/mdfc-attackpathsreco.png?raw=true)

6. Notice you can see that a publicly exposed VM that has a managed identity can read key vault. The path also gives you specifics of which VM and Key Vaults are potential targets.

   ![Attack Paths example scenario detail](../images/mdfc-attackpathexampledetail1.png?raw=true)

   > **Note**: To learn more about any particular Attack Path simply select it and explore it.

7. Select the **VM (1)** in the attack path, and click on **Recommendations (2)** you will see the vulnerabilities and any security recommendations that are relevant to this machine. 

   ![Attack Paths VM detail](../images/mdfc-attackpathvmedetail.png?raw=true)

8. Select an **Unhealthy** recommendation, you will see the remediation steps, and click on the **Take action** button at the bottom left of the screen you will see the screen where you can implement these remediations.

   ![Attack Paths VM detail](../images/mdfc-attackpathvmrecommendtiondetail.png?raw=true)

9. Now you have a complete picture of:
      - What resources can cause potential risk exposure.
      - What is a likely path that leads to exposure.
      - What are the open recommendations on these resources.
      - How to remediate open attack paths.

### Task 2: Building and exploring your own custom risk scenarios

1. From **Defender for Cloud** menu, open the **Cloud Security Explorer** page.

   ![Cloud Security Explorer](../images/m1-img6.png?raw=true)

2. Let's build our scenario where we will identify public vulnerable machines that can access object storage.

3. Choose **Internet exposed VMs with high severity vulnerabilities (1)** template from **Query Templates** and click on **Search (2)**.

   ![Cloud Security Explorer VM example](../images/select-query.png?raw=true)

4. You will see a list of machines that are not only publicly exposed but also vulnerable. Now, let's expand this to identify machines that have permissions to other resources (managed identities). 

5. Click on the **plus (1)** next to Virtual Machines (group), from the drop-down of **select Condition (2)** Select **Identity & Access (3)**, and select **Can authenticate as (4)**.

   ![Cloud Security Explorer Custom Scenario](../images/identity-authenticate.png?raw=true)

6. From the drop-down of **select resource group type (1)**, select **Application identities (2)**, click on **Done (3)**, and click on **plus (4)** next to Application identities (group).

    ![Cloud Security Explorer Custom Scenario](../images/identity-application.png?raw=true)

7. Now let's add the resource type to which this VM has access via managed identity. From the drop-down of **Select condition (1)**, select **Identity & Access (2)**, and select **Has permissions to (3)**.
   
    ![Cloud Security Explorer Custom Scenario](../images/identity-permission.png?raw=true)

8. Now you will need to select the type of resource that this VM can access using a managed identity. From the drop-down of **Select resource type (1)**, select **Object storage (2)**, and click on **Done**.

    ![Cloud Security Explorer Custom Scenario](../images/object-storage.png?raw=true)

9. Then click on **Search** button, and you will see a list of machines that can be the target of this attack path.

    ![Cloud Security Explorer Custom Scenario](../images/mdfc-cloudsecurityexplorersearchresults.png?raw=true). 

