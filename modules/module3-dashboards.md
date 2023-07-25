# Module 3 - Dashboards

<br>

Other than the overall dashboard we discussed in Module 1, MDC provides several purpose built reports, which are presented as Workbooks. 

![Workbooks](../Images/mdfc-workbooks.png?raw=true)

## Ransomware Dashboard

1. From the available workbooks select ***Ransomware Dashboard*** under **Community**. The page shows the state of your current environment against various MITRE Tactics used by ransomwares
![Ransomware Dashboard](../Images/mdfc-ransomwaredashboard.png?raw=true)
2. Select ***Recommendations*** to see technique specific recommendations ![Ransomware Recommendations](../Images/mdfc-ransomwarerecommendations.png?raw=true)
3. Select ***Discovery*** and ***Container and Resource Discovery*** ![Ransomware Recommendations](../Images/mdfc-ransomwarediscovery.png?raw=true)
4. You can filter the Techniques. We will leave ***All*** selected ![Ransomware Recommendations](../Images/mdfc-ransomwarefilter.png?raw=true)
5. Select ***asclab-aks*** under Resources and scroll to the right and click the ***Go to recommendation*** link under URL![Ransomware Recommendations](../Images/mdfc-ransomwarerecommendation.png?raw=true)
6. You will be taken to the recommendation details that contains remediation steps and an option to Fix ![Ransomware Recommendations](../Images/mdfc-ransomwarefix.png?raw=true)
7. Close the Workbook by clicking the X at the top right corner of screen


## Identifying the coverage of your attack surface

1. Select the ***Coverage*** workbook under **Community** 
   ![Coverage](../Images/mdfc-coverage.png?raw=true)
2. You can now see what Defender plans are enabled across different subscriptions
3. To select the settings of any plan for a given subscription click the ***on*** or ***off*** corresponding to the plan<br>
![Coverage](../Images/mdfc-planonoff.png?raw=true)
4. Now you can change the plan settings 
   ![Coverage](../Images/mdfc-plansettings.png?raw=true)


## Deploying community workbooks

In addition to the workbooks available in the Azure Portal, you can also deploy several from the [MDC github](https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Workbooks)

1. From the ***Workbooks*** blade select the ***Microsoft Defender for Cloud*** under Community Git Repo<br>
   ![Community Workbook](../Images/mdfc-github.png?raw=true)
2. You will be taken to the MDC Github page. Scroll down to bottom to select *WellArchitected Framework Security* <br>![Community Workbook](../Images/mdfc-waf.png?raw=true)
3. After selecting the workbook scroll down on the page until you see **Try it on the Azure Portal** and click the blue button *Deploy to Azure*<br>![Community Workbook](../Images/mdfc-waf2.png?raw=true)
4. Choose the subscription and create a new ***Resource Group*** and leave other settings unchanged. Press Review + create button at bottom left corner. On subsequent screen press **create**![Community Workbook](../Images/mdfc-webdeploy.png?raw=true)
5. Select Go to resource from the screen ![Community Workbook](../Images/mdfc-depcomplete.png?raw=true)
6. You will now get an option to open the workbook. Please go ahead and click on that button![Community Workbook](../Images/mdfc-wafwbdeploy-1.png?raw=true)
7. Now you will see the workbook, choose the Subscription Name as shown in fig below to see how that subscription scores against Well Architected Practices<br> ![Community Workbook](../Images/mdfc-waf-final.png?raw=true)

You can repeat this process to deploy other Workbooks from the community repo or any that you have created.
