# Module 1 - Exploring Microsoft Defender for Cloud


### Task 1: Understanding Microsoft Defender for Cloud Dashboard 

1. Open **Azure Portal** and search for **Microsoft Defender for Cloud (1)** and then click on it from the search results **(2)**.

    ![Microsoft Defender for Cloud](../images/M0-T1-S1.2.png)   

2. On the **Overview (1)** blade notes that it now provides a unified view into the security posture and includes multiple independent cloud security pillars such as **Security posture, Regulatory compliance, Workload protections, Firewall Manager, Inventory, and Information Protection (preview) (2)**. Each of these pillars also has its own dedicated dashboard allowing deeper insights and actions around that vertical, providing easy access and better visibility for security professionals.

   > **Info**: Microsoft Defender for Cloud takes time to populate information such as secure score, compliance, recommendations, etc. after enabling the services and enrolling the servers to Microsoft Defender for Cloud.
 
   ![Microsoft Defender for Cloud Snapshot](../images/M1-T1-S1.png)  


3. Note that  the **top menu** bar allows to view and filter subscriptions by selecting the **subscriptions button**. In this lab we will use only one but selecting different/additional subscriptions will adjust the interface to reflect the security posture for the selected subscriptions.

   ![Microsoft Defender for Cloud Snapshot](../images/M1-T1-S2.png)  

4. Click on the **What’s new** button – a new tab opens with the latest release notes where you can stay current on the new features, bug fixes, and more.

    ![Microsoft Defender for Cloud Snapshot](../images/M1-T1-S4.png)  
	
5. Note the **high-level numbers** at the top menu; This view allows you to see a summary of your subscriptions, active recommendations, and security alerts alongside connected cloud accounts.

    ![Microsoft Defender for Cloud: Top menu](../images/M1-T1-S5.png) 

6. From the top menu bar, **click** on **Azure subscriptions**.
	
    ![Microsoft Defender for Cloud: Coverage](../images/M1-T1-S6.png)

    - This will bring you into the environment settings. Then select the available subscription. 

   	![Microsoft Defender for Cloud: Coverage](../images/M1-T1-S6.1.png)

7. On the **Defender plans** page, note that your subscription is fully covered – which means that your subscription is covered by Microsoft Defender for Cloud. 	

    ![Microsoft Defender for Cloud: Coverage](../images/defender1.png)

    > **Info**: This page shows a list of subscriptions and their coverage type. You can use this page to find subscriptions that are not covered by Microsoft Defender for Cloud and help you identify “shadow IT” subscriptions.

8. Go back to the **Overview** page, and look at the **Secure Posture** tile, you can see your current score along with the number of completed controls and recommendations. Clicking on this tile will redirect you to a drill-down view across subscriptions.

    ![Overview: Secure Score tile](../images/M1-T1-S8.png)

    > **Info**: The higher the score, the lower the identified risk level.

9. On the **Regulatory Compliance (1)** tile, you can get insights into your compliance posture based on continuous assessment of both Azure and hybrid cloud environments. This tile shows the following standards which are **Azure Security Benchmark(2)**, and **Lowest compliance regulatory standard (3)** to view the data we first need to add **Security policies**. 
 
     > Clicking on this tile will redirect you to the Regulatory Compliance dashboard – where you can add additional standards and explore the current ones. 

     ![Overview: Regulatory Compliance tile](../images/regcomp.png)
   
10. Navigate to **Environment settings (1)**, select the available **Subscription (2)**. 

     ![Overview: Regulatory Compliance tile](../images/sub.png)

11. From the **Environment settings** page navigate on **Security policy (1)** and click on **Add more standards (2)** under **Industry & regulatory standards**.

     ![Overview: Regulatory Compliance tile](../images/security.png)

12. On the **Add regulatory compliance standards** page click on **Add** next to **ISO 27001:2013** standard.

     ![Overview: Regulatory Compliance tile](../images/security.png)

13. On the **ISO 27001:2013** assign initiative page click on **Review + Create**.

     ![Overview: Regulatory Compliance tile](../images/isoreviewcreate.png) 

14. Click on **Create**.

     ![Overview: Regulatory Compliance tile](../images/isocreate.png) 

15. Now on the **Security policy** page, click on **Add more standards** under **Industry & regulatory standards** and select **PCI DSS 4** standard and click on **Add**.

     ![Overview: Regulatory Compliance tile](../images/pci.png) 

16. On the **PCI DSS 4** assign initiative page click on **Review + Create**.

     ![Overview: Regulatory Compliance tile](../images/pcireviewcreate.png) 

17.  Click on **Create**.

     ![Overview: Regulatory Compliance tile](../images/pcicreate.png)

     
18. Now on the **Security policy** page, click on **Add more standards** under **Industry & regulatory standards** and select **SOC 2** standard and click on **Add**.

     ![Overview: Regulatory Compliance tile](../images/soc.png) 

19. From the **SOC 2 Type 2** assign initiative page basic tab navigate to **Parameters** tab.

     ![Overview: Regulatory Compliance tile](../images/socpara.png) 

20. On the **Parameters** tab enter the following parameters and click on **Review + Create (4)**.

	- Allowed registry or registries regex: **[] (1)**
 	- Max allowed CPU units: **200m (2)**
   	- Max allowed memory bytes: **1 (3)** 

     ![Overview: Regulatory Compliance tile](../images/parasoc.png) 

21.  Click on **Create**.

     ![Overview: Regulatory Compliance tile](../images/soccreate.png)

22. Navigate back to **Regulatory Compliance** to view the recently added standards click on **Show all 4**.

  > **Note**: It can take up to two hours for newly added standards to appear under the **Lowest compliance regulatory standard**. Please move on to the next step; you can review the standards later.

   ![Overview: Regulatory Compliance tile](../images/regulatory.png)


22. On the **Workload Protections** **(1)**, under Cloud Security, you can see the coverage of your **connected resources(2)** for the currently selected subscription. Your current resource coverage should be **fully covered 100% (3)** which means **full protection**. Additionally, you can also view the recent **security alerts (4)**, color-coded by severity.

     ![Overview: Microsoft Defender  for Cloud tile](../images/dfc5.png)

23. Next Click on **Inventory** from the **General** section of the Microsoft Defender for Cloud. It shows the number of unmonitored VMs alongside the total covered resources - **you should expect to have zero unmonitored VMs**. Resources are classified according to their health status.

     > Info: 
     > Unmonitored VMs are considered virtual machines that have a Log Analytics agent deployed, but the agent isn't sending data or has other health issues.

    ![Overview: Secure Score tile](../images/msdefender5.1.png)   


### Task 2: Exploring Secure Score and Recommendations 

Previously, we briefly explored the Secure Score tile on the overview page. Now let’s dive into this capability and the associated recommendations. Microsoft Defender for Cloud continually assesses your resources. All findings are aggregated into a single score (Secure Score) which measures the current security posture of your subscription; the higher the score, the lower the identified risk level.


1. In the **Microsoft Defender for Cloud Overview blade**. From the left navigation pane, under the **Cloud Security** section, click on the **Security posture** button.

    ![Overview: Secure Score tile](../images/M1-T2-S1.png) 

2. On the Secure Score page, **review your current overall secure score percentrage**.

	> **Note**: Your score is shown as a percentage value, but you can also see the number of points on which the score is being calculated based on. 

    ![Overall Secure Score](../images/dfc6.png)


   > For more information on how the score is calculated, [refer to the secure score documentation page](https://docs.microsoft.com/en-us/azure/security-center/secure-score-security-controls#how-your-secure-score-is-calculated).


3. On the bottom part, you can see a list of subscriptions and their current score. To view the recommendations behind the score, click on **view recommendations**.


### Task 3: Exploring Security Controls and Recommendations 

1. On the **Recommendations (1)** page, pay attention to the first part of the page; the **summary view (2)** which includes the current score, progress on the recommendations (both completed security controls and recommendations) and resource health (by severity).

    ![Overall Secure Score](../images/M1-T2-S3.png)

2. On the top menu, click on the **Download CSV report** button – this allows you to get a snapshot of your resources, their health status, and the associated recommendations. You can use it for pivoting and reporting.

     ![Overall Secure Score](../images/M1-T3-S3.png)

3. Under **Recommendation**, Click on **Manage access and permissions** and select **Storage account public access should be disallowed** from the drop down list.

     ![](../images/M1-T3-S6.1.png)

4. On the top section, notice the following:

   - Title of the recommendation: **Storage account public access should be disallowed**
   - Top menu controls: **Exempt**, **Deny**, **View policy definition** and **Open query**
   - Severity indicator: **Medium**
   - Freshness interval: **30 Min** 
   - Tactics and techniques: **Initial Access**

   ![Recommendation top menu](../images/stacc-public-access.png)

5. The next important part is the **Remediation Steps** which contains the remediation logic where you can remediate the selected resource/s.

6. Under **Affected resources**, **select a resource** (the single **storage account** on the Unhealthy resources) and click on **Fix**. This will automatically apply the remediation on the selected resource.

     ![](../images/affectedresources.png)
  
11. This will open a new window - **Fixing resources**, review the implications for this remediation and click on **Fix 1 resource**.

     ![](../images/ex2.step13.png)
  
12. Wait for a notification: ✅ **Remediation successful** - Successfully remediated the issues on the selected resources. 
    
    > **Note**: It can take several minutes after remediation completes to see the resources in the 'healthy resources' tab. You can move to the next task and come back later to check on this.

    > **Info**: In the recommendation list, you can now see some recommendations flagged as in the preview. They aren’t included in the calculation of your score. They should be still remediated so that when the preview period ends, they will contribute towards your final score.


### Task 4: Exploring the Inventory capability

Asset inventory dashboard allows you to get a single pane of glass view of all your resources covered by Microsoft Defender for Cloud. It also provides per-resource visibility to all Microsoft Defender for Cloud’s information and additional resource details including security posture and protection status. Since this dashboard is based on Azure Resource Graph (ARG), you can run queries across subscriptions at a large scale, quickly and easily.

1. Type **Microsoft Defender for Cloud** in the search box located on the top of the **Azure Portal** page and click to open it. From the left navigation pane, under the **General** section, select the **Inventory** button.

     ![](../images/inventory1.png)
    
2. Hover to the **Summaries strip** at the top of the page.

     ![](../images/inventory1.1.png)

    > **Note**: In your environment, these numbers may not be the same, since it varies in time

3. Notice the total number of resources, The total number of resources are the ones that are connected to the Microsoft Defender for Cloud and NOT the total number of resources that you have in your subscriptions.

4. Notice the number of **unhealthy resources**, The unhealthy resources are the resources with actionable recommendations based on the selected filter.

5. Notice the **unmonitored resources**, The unmonitored resources indicate if there are resources with the Log Analytics agent deployed but with health issues. Since we enabled the auto-provisioning in the previous module, all existing VMs are covered and connected, which means they are monitored.

6. Use the **Filter by name** box to search for **linux** **(1)**. You should now see a filtered view containing your desired resource: **asclab-linux**. Hover on the red bar in the **recommendations** column to see a tooltip with the **active recommendations (2)**. You should expect to see **Active-xx of xx Recommendations** – these are the active recommendations you must attend.

    ![linux-recommendations](../images/ex3.step7.png)

7. Open the resource health pane by selecting the resource. Click on **asclab-linux**. Alternately. you can also right-click on any resource and select **view resource**. You may not see **view resource** directly due to different screen resolutions, then you have to click on ellipse(...) and then select **view resource**.

    ![Remediate a resource](../images/viewres.png)

8. On the resource health pane for **asclab-linux**, review the virtual machine information alongside the recommendation list.

    ![Remediate a resource](../images/healthpreview.png)

    > **Note**: It could take up to 24 hours for all the recommendations to show up. And it is possible that during lab time, this may not show up – which is the case sometimes. If you don't see the data in **recommendations**. You can continue to the next exercise and verify this later.

9. Navigate back to the Inventory page and clear the search keyword **linux**. Then from the filter menu, select the **Resource Groups (1)** filter and from the deop-down menu of **value** select **asclab-aks (2)** (Unselect remaining), and click on **Ok (3)**. Using this filter, you can see all resources related to the predefined Kubernetes resources which are monitored with active recommendations.

     ![Remediate a resource](../images/filter-rg.png)

    > **Note:** The list can be filtered and sorted.

10. From the filter menu, select the **Resource Group** filter and **select all** under the Value. Again from the filter menu, select **Recommendations**, uncheck the **select all** option under the Value, and then select the **Auditing on SQL Server should be enabled** and click on **Ok**. You can also use the search area within the filter to better find across the list. When you are done exploring remember to clear your filter.

    > **Note**: If you don't see **Auditing on SQL Server should be enabled** in search results that means it is not loaded yet to recommendations and it could take up to 24 hours for all the recommendations to show up. It is possible that during lab time, this may not show up – which is the case sometimes. If you don't see the data in **Recommendations**, you can note down this step number then continue to the next exercise and verify this later.

11. Tags are a very common asset management feature within Azure. With the help of this feature, resources can be tagged using a Tag name and value. These assigned tags can organize your assets and categorize them with the help of filters. Let us now assign the following Tags:

	* Filter the **Resource type** column to include only **App Services or web services**: Select the **Resource type** filter and select **Web apps** under the Value and Click on **OK**
	* **Select** the checkboxes of the two app services named *asclab-fa-xx* and *asclab-app-xx*. (Here **xx** is the unique id of the resource).
	* From the top menu, click **Assign tags**
	* Assign `Environment` as the name and  `Production` as the value.
	* Click **Save**.

	> **Note**: If you don't see App Services in the Resource type filter that means it is not loaded yet to recommendations, Note down this step number and verify this later.

	![Inventory: Assign tags](../images/defassigntag.gif?raw=true)
   
12. From the filter pane, remove the **Resource type** filter then go to **Add filter** and notice the **Security findings** filter – it allows you to find all resources that are prone to a specific vulnerability. You can also search for CVE, KB ID, name, and missing update.

13. From the filter pane, remove the **Security findings** filter if you added in the previous step then from the top menu, click on **Open query**.

    ![Inventory: Assign tags](../images/inventory-open-query-new.1.png)

16. On the **Azure Resource Graph Explorer** blade, click on **Run Query**. You should now have the same list of resources and columns as in the previous step. This query is editable for your needs and here it gets very powerful.
 
    ![Inventory: Assign tags](../images/run-query.1.png)

17. Save the query for later use by clicking on **Save as** from the top menu. You can use it to create periodic reports. Name the report as *asc-filtered-query* and select **save**.

    ![Inventory: Assign tags](../images/M2-EX3-17.png)



### Task 5: Understanding pricing

The pricing criteria depends on the plan you enable. In addition, as a part of Foundational CSPM (free), you get several items like Secure Score, Asset Inventory, Security Recommendations, etc.

Refer the following to learn more about Defender for cloud pricing:

 - [Pricing Page](https://azure.microsoft.com/en-us/pricing/details/defender-for-cloud/?v=17.23h)

 - [Foundational CSPM vs. Defender CSPM capabilities](https://learn.microsoft.com/en-us/azure/defender-for-cloud/concept-cloud-security-posture-management)


1. From **Microsoft Defender for Cloud**, click on **Workbook (1)** select **Public Template (2)** tab and click on **Cost Estimation (3)** 

    ![MDC pricing](../images/costdefnder.png)

2. In the **Cost Estimation** workbook, you can observe the estimated pricing for the resources.

    ![MDC pricing](../images/costworkbook.png)
   

### Task 6: Overview of CWP capabilities  (Read Only) 

1. Navigate to **Workload protections** from the **Cloud Security** section of **Defender for Cloud** menu to view the **Workload Protections Dashboard**.

    ![MDC pricing](../images/defendercwpdashboard.png)

   ***The dashboard includes the following sections:***

	- **Microsoft Defender for Cloud coverage (1)** - Here you can see the resources types that's in your subscription and eligible for protection by Defender for Cloud. Wherever relevant, you can upgrade here as well. If you want to upgrade all possible eligible resources, select Upgrade all.

	- **Security alerts (2)** - When Defender for Cloud detects a threat in any area of your environment, it generates an alert. These alerts describe details of the affected resources, suggested remediation steps, and in some cases an option to trigger a logic app in response. Selecting anywhere in this graph opens the Security alerts page.

 	- **Advanced protection (3)** - Defender for Cloud includes many advanced threat protection capabilities for virtual machines, SQL databases, containers, web applications, your network, and more. In this advanced protection section, you can see the status of the resources in your selected subscriptions for each of these protections. Select any of them to go directly to the configuration area for that protection type.

	- **Insights (4)** - This rolling pane of news, suggested reading, and high priority alerts gives Defender for Cloud's insights into pressing security matters that are relevant to you and your subscription. Whether it's a list of high severity CVEs discovered on your VMs by a vulnerability analysis tool, or a new blog post by a member of the Defender for Cloud team, you'll find it here in the Insights panel.
