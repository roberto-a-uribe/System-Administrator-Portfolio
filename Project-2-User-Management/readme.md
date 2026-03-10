# Project 2 – Active Directory User and Group Management


## Overview

This project involved creating AD users and groups, modifying different attributes of AD users and AD groups in a home lab using Windows ADUC and Powershell script within domain called "BERTO.local".



## Step 1 - Created Single/Multiple end users
User creation - Clark Kent
- Single user creation using powershell script**
    
- ![Project-2-User-Management](PS-ckent-cmd-verified.png "My Project Logo")
  
- ![Project-2-User-Management](PS-ckent-ADUC-verified.png "My Project Logo")



## Encountered Powershell ERROR / Resolution

Ran powershell script and ERROR came up - after error checking and troubleshooting - Error stemmed from wrong input of OU (Org Unit) designation instead of CN (Common Name) as per domain ADUC structure within the powershell script.


- ![Project-2-User-Management](PS-new-aduser-ERROR.png "My Project Logo")
  


## Step2 - User Creation - Bulk addition

Ran powershell script to create bulk users from a csv file which included several attributes.


- ![Project-2-User-Management](PS-new-adusers-bulk-creation.png "My Project Logo")
- ![Project-2-User-Management](CSV-list-new-adusers-bulk-creation.png "My Project Logo")

- Verified bulk users were created by a poweshell check and ADUC structure.
  
- ![Project-2-User-Management](PS-new-adusers-bulk-check.png "My Project Logo")
- ![Project-2-User-Management](ADUC-new-adusers-bulk-creation.png "My Project Logo")
  



## Step 3 - AD Group creation and User assignment




## Skills Demonstrated

- OU design for scalable AD structure
- User account provisioning in Active Directory
- Security group creation and access modeling
- GUI-based AD administration using ADUC
- PowerShell verification of AD group membership
