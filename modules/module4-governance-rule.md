# Module 4 - Governance Rule

Governance rules can identify resources that require remediation according to specific recommendations or severities. The rule assigns an owner and due date to ensure the recommendations are handled. Many governance rules can apply to the same recommendations, so the rule with lower priority value is the one that assigns the owner and due date.

### Task 1: Assign Governance Rule

1. From **Defender for Cloud** menu, click on **Environment Settings (1)** page and select your subscription **(2)**.

    ![](../images/m1-img2.png)

2. Under **Policy settings** Select **Governance Rules (1)** and click on **Enter the new experience (2)**.

    ![](../images/m1-img19.png)

3. Click on **+ Create governance rule**.

    ![](../images/m1-img20.png)

4. Enter **Rule name** as `asclab-rule` **(1)**, select **Scope** at subscription level **(2)** and **Priority** `100` **(3)**. Click **Next (4)**.

    ![](../images/m1-img21.png)
    
5. Under **conditions** provide the below details and click **Create (5)**
	
   - **By severity**: `High` **(1)**
   - **Owner**: `By email address` **(2)**
   - **Email address**: <inject key="AzureAdUserEmail"></inject> **(3)**
   - **Remediation timeframe**: `90 days` **(4)**

    ![](../images/m1-img22.png)

6. On the **Rule created succsessfuly** pop-up select the check box next to **Apply rule to the existing recommendations that are unassigned** and click on **Ok**.

    ![](../images/a1.6.png)

7. Click on **Governance report** to view the status of tasks **Complete, Ontime and Unassign**.

    ![](../images/m1-img23.png)
    
    ![](../images/m1-img24.png)

