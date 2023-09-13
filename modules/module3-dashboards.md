# Module D - Dashboards

## Overview

Other than the overall dashboard we discussed in Module 1, Microsoft Defender for Cloud provides several purpose built reports, which are presented as Workbooks. 

### Task 1: Ransomware Dashboard

1. From the available **Workbooks (1)** select **Ransomware Dashboard (2)** under **Community**. The page shows the state of your current environment against various MITRE Tactics used by ransomwares.
   
   ![Workbooks](../images/M3-T1-S1.1.png)

2. Ransomware Dashboard is navigated. 
                                                                                                                     
   ![Ransomware Dashboard](../images/M3-T1-S1.png)

3. Select **Recommendations** to see technique specific recommendations.

   ![Ransomware Recommendations](../images/M3-T1-S2.png)

4. Select **Discovery (1)** and **Container and Resource Discovery (2)**.

   ![Ransomware Recommendations](../images/M3-T1-S3.png)

5. You can filter the Techniques. We will leave **All** selected.

   ![Ransomware Recommendations](../images/M3-T1-S4.png)

6. Click on expand grid **(1)**, next under **Discover (2)** section, select **asclab-aks (3)** and click the **Go to recommendation (4)** link.

    ![Ransomware Recommendations](../images/dfc7.png)

7. You will be taken to the recommendation details that contains remediation steps and an option to Fix.

    ![Ransomware Recommendations](../images/M3-T1-S6.png)

8. Close the Workbook by clicking the **X** at the top right corner of screen.


### Task 2: Identifying the coverage of your attack surface

1. Under **Workbooks (1)**, Select the **Coverage (2)** workbook.

   ![Coverage](../images/M3-T2-S1.1.png)

2. You can now see what Defender plans are enabled across different subscriptions.

   ![Coverage](../images/M3-T2-S2.1.png)

3. To select the settings of any plan for a given subscription click the **on** or **off** corresponding to the plan.

   ![Coverage](../images/M3-T2-S3.png)

4. Now you can change the plan settings.

    ![Coverage](../images/defender1.png)


### Task 3: Deploying community workbooks

In addition to the workbooks available in the Azure Portal, you can also deploy several from the [MDC github](https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Workbooks)

1. From the **Workbooks (1)** blade select the **Microsoft Defender for Cloud (2)** under Community Git Repo.

   ![Community Workbook](../images/M3-T3-S1.png)

2. It will navigate to the **MDC Github** page. Scroll down to bottom to select **WellArchitected Framework Security**.

   ![Community Workbook](../images/M3-T3-S2.png)

3. In the workbook, scroll down on the page until you see **Try it on the Azure Portal** and click the blue button **Deploy to Azure**.

   ![Community Workbook](../images/M3-T3-S3.png)

4. Choose the **subscription (1)** and select **asclab-WAF (2)** for **Resource Group** from the dropdown and leave other settings unchanged. Press **Review + create (3)** button at bottom left corner. On subsequent screen press **Create**.

   ![Community Workbook](../images/M3-T3-S4.png)

5. Once deployment is completed, select **Go to resource** from the screen.

   ![Community Workbook](../images/M3-T3-S5.png)

6. Click on **Open Workbook**.
   
   ![Community Workbook](../images/M3-T3-S6.png)

7. Now you will see the workbook, choose the **Subscription Name** to see how that subscription scores against **Well Architected Practices**.

    ![Community Workbook](../images/M3-T3-S7-1.png)


>**Note**: You can repeat this process to deploy other Workbooks from the community repo or any that you have created.
