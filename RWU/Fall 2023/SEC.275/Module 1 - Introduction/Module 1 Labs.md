---
aliases:
  - "20230901111410"
tags:
  - TestOutServer
  - SEC
  - SEC275
date_created: 2023-09-01 11:14
Index: "[[SEC.275 Index]]"
---
# Module 1 Labs
---
## 1.2.4 Use the Windows Client Interface
### Lab Prompt
In this lab, you will explore the features of the Windows 10 user interface. You need to complete a specific task in each area you visit. Be sure to complete every task for full credit on the lab.

Complete this lab as follows:

1. Configure the screen saver settings.
    1. Right-click **Start** and then select **Settings**.
    2. Maximize the window for better viewing.
    3. Select **Personalization**.
    4. From the left pane, select **Lock screen**.
    5. From the right pane, scroll down and select **Screen saver settings**.
    6. Under Screen Saver, use the drop-down to select **Photos**.
    7. Configure the **Wait** time to **5** minutes.
    8. Select **On resume, display logon screen**.
    9. Select **OK** to close the Screen Saver Settings dialog.
    10. In the top left, select **Home** to return to the Windows Settings page.
2. Check for Windows updates.
    1. From Windows Settings app, select **Update & Security**.
    2. Select **Check for updates**.
    3. In the top right, select **Answer Questions**.
    4. Answer Question **1**.
    5. Minimize the Lab Questions dialog.
    6. In the top left of the Settings app, select **Home** to return to the Windows Settings page.
3. Install the SalesPrinter attached to the CorpFiles16 server and then set it as your default printer.
    1. From Windows Settings app, select **Devices**.
    2. From the left pane, select **Printers & scanners**.
    3. From the right pane, select **Add a printer or scanner**.
    4. Select **SalesPrinter on CorpFiles16**.
    5. Select **Add device**.
    6. After the printer has been installed, under _Printers & scanners_, select **SalesPrinter on CorpFiles16**.
    7. Select **Manage**.
    8. Select **Set as default**.
    9. In the top left, select the **Home icon** to return to the Windows Settings page.
4. Enable Remote Desktop.
    1. From Windows Settings app, select **System**.
    2. From the left pane, select **Remote Desktop**.
    3. From the right pane, under Enable Remote Desktop, slide the switch to **On**.
    4. Select **Confirm**.
    5. In the top left, select **Home** to return to the Windows Settings page.
5. Enable a network adapter.
    1. From Windows Settings app, select **Network & Internet**.
    2. From the left pane, select **Ethernet**.
    3. From the right pane, select **Change adapter options**.
    4. Right-click **Ethernet** and select **Enable**.
    5. Close the Network Connections window.
    6. Close the Settings app.
6. Use PowerShell to identify the network addresses and routes.
    1. Right-click **Start** and select **Windows PowerShell (Admin)**.
    2. Maximize the window for better viewing.
    3. From the PowerShell prompt, type **ipconfig /all** and then press **Enter**.
    4. View the **IP addresses** set for the default gateway and the DNS Servers.
    5. From the PowerShell prompt, type **ping 192.168.0.5** and then press **Enter** to ping the gateway.
    6. In the top right, select **Answer Questions**.
    7. Answer Question **2**.
    8. From the PowerShell prompt, type **tracert 163.128.78.93** and then press **Enter** to discover the path to the external DNS server.
    9. From the Lab Questions dialog, answer Question **3**.
    10. Minimize the Lab Questions dialog.
    11. Close the PowerShell window.
7. Use File Explorer to create a folder named Reports.
    1. Right-click **Start** and select **File Explorer**.
    2. From the left pane, select **This PC**.
    3. From the right pane, double-click **Data (D:)** to open this drive.
    4. From the right pane, right-click in the white space and select **New** > **Folder**.
    5. In the Name field, type **Reports** and then press **Enter**.
    6. Close File Explorer.
8. Optimize the C: drive.
    1. Select **Start**.
    2. Select the letter **A** to access the alphabetic options.
    3. Select the letter **W** to jump to the W section of the Start menu.
    4. Expand and select **Windows Administrative Tools** > **Defragment and Optimize Drives**.
    5. Select **System (C:)**.
    6. Select **Optimize**.  
        Viewing the _Current Status_ column, watch the optimization process run.
    7. Upon completion, select **Close**.
9. Configure the default minimum password length to 10 characters.
    1. Select **Start**.
    2. Scroll down and select **Windows Administrative Tools** and then select **Local Security Policy**.
    3. From the left pane, expand and select **Account Policies** > **Password Policy**.
    4. In the middle pane, double-click **Minimum password length**.
    5. Increase the value to **10** characters and then select **OK**.
    6. Close the Local Security Policy console.
10. Use Computer Management to configure the _Application Identity_ service.
    1. Right-click **Start** and then select **Computer Management**.
    2. Maximize the window for better viewing.
    3. From the left pane, expand and select **Services and Applications** > **Services**.
    4. (Optional) For easier viewing, you can select the **Standard** tab at the bottom.
    5. From the middle pane, double-click the **Application Identity** service.
    6. Using the _Startup type_ drop-down, select **Automatic** to allow the service to start automatically at boot.
    7. Under _Service status_, select **Start** to start the service.
    8. Select **OK**.
    9. Close Computer Management.
11. Score the lab.
    1. In the top right, select **Answer Questions**.
    2. Select **Score Lab**.

### Solution
![[Screenshot 2023-09-01 at 11.25.26 AM.png]]
![[Screenshot 2023-09-01 at 11.25.44 AM.png]]
- Explanation is found in lab prompt

---
## 1.2.7  - Use the Windows Server Interface
### Lab Prompt
In this lab, you will explore the Windows Server 2022 user interface. Windows Server 2022 starts in the desktop view with Server Manager open.

Complete this lab as follows:

1. Clean up system files.
    1. From Server Manager, select **Tools** > **Disk Cleanup**.
    2. From the _Disk Cleanup: Drive Selection_ window, verify that **System (C:)** is selected and then select **OK**.
    3. From the Disk Cleanup tab, under _Files to delete_, leave all items currently marked as-is and then place a checkmark in each of the following:
        - Microsoft Defender Antivirus
        - Windows error reports and feedback
        - DirectX Shader Cache
        - Delivery Optimization Files
        - Setup Log files
        - System queued Windows Error Reporting
    4. Select **OK**.
    5. Select **Delete Files**.
2. Launch Windows PowerShell and run **tracert**.
    1. Right-click **Start** and then select **Windows PowerShell**.
    2. At the PowerShell prompt, type **tracert 163.128.80.93** and then press **Enter** to discover the path to the external DNS server. Each router in the path to the DNS server is displayed.
    3. From the top right, select **Answer Questions**.
    4. Answer Question 1.
    5. Minimize the Lab Questions dialog.
    6. Close the PowerShell window.
3. Turn off the display in one hour.
    1. Right-click **Start** and then select **Power Options**.  
        The _Settings_ app is opened to the _Power & sleep_ page.
    2. Under _Screen_, use the drop-down to select **1 Hour**.
4. Modify adapter settings.
    1. From the top left of the Settings app, select **Home**.
    2. Select **Network & Internet settings**.
    3. From the right pane, select **Change adapter options**.  
        Notice that there are several real and several virtual network adapters.
    4. Right-click **vEthernet (External)** and select **Properties**.
    5. Select **Internet Protocol Version 4 (TCP/IPv4)** and then select **Properties**.
    6. Change the subnet mask to **255.255.255.0** and then select **OK**.
    7. Select **Close**.
    8. Close Network Connections.
5. Adjust the display setting.
    1. From the top left of the Settings app, select **Home**.
    2. Select **System**.
    3. From the left pane, scroll down and select **About**.
    4. Maximize the windows for better viewing.
    5. From the right pane, scroll down and under _Related settings_ select **Advanced system settings**.
    6. From the _Advanced_ tab, under Performance, select **Settings**.
    7. Select **Adjust for best performance** and then select **OK**.
    8. Select **OK** to close System Properties.
    9. Close the System window.
    10. From the top right, select **Answer Questions**.
    11. Select **Score Lab**.

After you have completed all of the assigned tasks, feel free to explore the operating system interface in the lab. When you are ready to end the lab, from the top right, select **Answer Questions** and then select **Score Lab**.  
To score 100% on the lab, make sure that all assigned tasks are complete before you select **Score Lab**.

### Solution
![[Screenshot 2023-09-01 at 11.37.02 AM.png]]
- Explanation is just the lab prompt again
---
## 1.2.10 - Use the Azure Interface
### Prompt
You are the network administrator for your company. You have decided to begin the configuration of Azure to help manage your network. You need to create a resource group to organize your Azure assets.

In this lab, your task is to create a resource group using the following information:
- Azure portal:
    - Site: **http://portal.azure.com**
- Project details:
    - Subscription name: **CorpNet Production**
    - Resource group name: **CorpNetCloud**
- Resource details:
    - Region: **(US) West US2**

### Solution
![[Screenshot 2023-09-01 at 11.59.00 AM.png]]

---
