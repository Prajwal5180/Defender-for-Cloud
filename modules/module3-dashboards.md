# Exercise 4 - Ransomware Dashboard and Identifying the coverage of your attack surface

## Overview

Other than the overall dashboard we discussed in Module 1, Microsoft Defender for Cloud provides several purpose-built reports, which are presented as workbooks.

### Task 1: Ransomware Dashboard

1. From the available **Workbooks (1)**, select **Ransomware Dashboard (2)** under **Community**. The page shows the state of your current environment against various MITRE tactics used by ransomware.
   
   ![Workbooks](../images/M3-T1-S1.1.png)

2. The Ransomware Dashboard is navigated.
                                                                                                                     
   ![Ransomware Dashboard](../images/M3-T1-S1.png)

3. Select **Recommendations** to see technique-specific recommendations.

   ![Ransomware Recommendations](../images/M3-T1-S2.png)

4. Select **Discovery (1)** and **Container and Resource Discovery (2)**.

   ![Ransomware Recommendations](../images/M3-T1-S3.png)

5. You can filter the techniques. We will leave **All** selected.

   ![Ransomware Recommendations](../images/M3-T1-S4.png)

6. Click on expand grid **(1)**, next under the **Discover (2)** section, select **asclab-aks (3)**, and click the **Go to recommendation (4)** link.

    ![Ransomware Recommendations](../images/dfc7.png)

7. You will be taken to the recommendation details that contain remediation steps and an option to fix.

    ![Ransomware Recommendations](../images/M3-T1-S6.png)

8. Close the workbook by clicking the **X** at the top right corner of the screen.


### Task 2: Identifying the coverage of your attack surface

1. Under **Workbooks (1)**, select the **Coverage (2)** workbook.

   ![Coverage](../images/M3-T2-S1.1.png)

2. You can now see what Defender plans are enabled across different subscriptions.

   ![Coverage](../images/M3-T2-S2.1.png)

3. To select the settings of any plan for a given subscription, click the **on** or **off** corresponding to the plan.

   ![Coverage](../images/M3-T2-S3.png)

4. Now you can change the plan settings.

    ![Coverage](../images/defender1.png)


### Task 3: Deploying community workbooks

In addition to the workbooks available in the Azure Portal, you can also deploy several from the [MDC github](https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Workbooks)

1. From the **Workbooks (1)** blade, select the **Microsoft Defender for Cloud (2)** under Community Git Repo.

   ![Community Workbook](../images/M3-T3-S1.png)

2. It will navigate to the **MDC Github** page. Scroll down to the bottom to select **WellArchitected Framework Security**.

   ![Community Workbook](../images/M3-T3-S2.png)

3. In the workbook, scroll down on the page until you see **Try it on the Azure Portal** and click the blue button **Deploy to Azure**.

   ![Community Workbook](../images/M3-T3-S3.png)

4. Choose the **subscription (1)** and select **asclab-WAF (2)** for **Resource Group** from the dropdown, leaving other settings unchanged. Press the **Review + Create (3)** button at the bottom left corner. On the subsequent screen, press **Create**.

   ![Community Workbook](../images/M3-T3-S4.png)

5. Once deployment is completed, select **Go to resource** from the screen.

   ![Community Workbook](../images/M3-T3-S5.png)

6. Click on **Open Workbook**.
   
   ![Community Workbook](../images/M3-T3-S6.png)

7. Now you will see the workbook, choose the **Subscription Name** to see how that subscription scores against **Well Architected Practices**.

    ![Community Workbook](../images/M3-T3-S7-1.png)


>**Note**: You can repeat this process to deploy other Workbooks from the community repo or any that you have created.

   > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   > - Navigate to the Lab Validation Page, from the upper right corner in the lab guide section.
   > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
   > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.
