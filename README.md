

```markdown
# AD_HealthCheck

Script to check the health of your Active Directory environment.

The latest version available online was v1.14. This repository contains updated versions with several modifications and enhancements.

---

## Main Modifications

- v1.15 (2019-11-22): Adjusted hash tables for PowerShell v3 and above, updated gpotool to the latest version.  
- v1.16 (2019-11-26): Added parameter to choose between verifying Forest or Domain, added option to send email.  
- v1.17 (2020-08-18): Adjusted script to run gpotool in Forest or Domain mode.  
- v1.18 (2020-12-10): Adjusted embedded images to be sent by email and added a boolean variable to choose whether to send email or not.  

---

## How to Use the Script

Place the following files in the same folder:

- AD_Configuration.xsd  
- AD_Configuration.xml  
- gpotool.exe  
- AD_Health_Check_v1.18_Git.ps1  

### Permissions Required
Create a service account with Domain Admin permissions to run this script properly.

### Files Description

- AD_Health_Check_v1.18_Git.ps1 – Main script.  
- AD_Configuration.xml – XML configuration file where you define your PDC, Schema Master, RID Master, Infrastructure Master, Naming Master, Sites, Subnets, and Links.  
- gpotool.exe – Group Policy verification tool. More information: https://www.windowstechno.com/group-policy-verification-tool-gpotool-exe/  
- ADHC_Auxiliar_XML.xlsx – Worksheet to assist in filling the XML after the first execution.  
- Button-Blank-Gray-icon.png, Button-Blank-Green-icon.png, Button-Blank-Red-icon.png, Button-Blank-Yellow-icon.png – Status icons. These should be placed in a subfolder named Images at the same level as the main script.  

---

## Output Information

When running the script for the first time, the HTML output will display information about Sites, Subnets, Adjacent Sites, and Site Links.  
These items will initially appear in yellow. After updating AD_Configuration.xml with the correct details, subsequent runs will display them in green, and any changes will be highlighted.  

The provided worksheet ADHC_Auxiliar_XML.xlsx can be used to organize the required data before pasting it into the XML configuration file.

---

## Maintainer

Maintained by: komezino2021  
Email: clementsadjere@gmail.com  
