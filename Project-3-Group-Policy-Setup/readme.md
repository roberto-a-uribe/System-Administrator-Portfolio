# Project 3 – Group Policy Setup & Configuration

## Overview


This project involved configuring and applying group policy settings to designated users and groups within home lab Active Directory (`BERTO.local`).
In this lab I walk through every key step—from understanding GPO concepts to installing tools, creating policies, and applying them.

## 🛡️ Group Policy Management Home Lab: Creating and Setting Up GPOs





### 🧠 What is GPO?

**Group Policy Object (GPO)** is a feature of Microsoft Windows Active Directory that provides centralized management and configuration of operating systems, applications, and users' settings.


GPOs allow administrators to:

* Enforce password policies
* Configure desktop environments
* Install software
* Set user rights
* Restrict access to certain features or areas

---

### 📚 GPO Review

This section offers a quick theoretical review of Group Policy concepts:

* **Local GPO**: Applies settings to the local machine
* **Non-local GPO**: Created in AD DS and applies to users/computers in OUs
* **Group Policy Inheritance**: Policies are inherited from parent OUs unless blocked
* **Policy Precedence**: Local < Site < Domain < OU

GPO settings are divided into:

* **Computer Configuration**: Applied during system startup
* **User Configuration**: Applied at user login

---

### 🛠️ Installing the Group Policy Management Console (GPMC)

To manage GPOs, the **GPMC** must be installed.

#### Step 1:
On the domain controller:

   * Open **Server Manager**
   * Click **Add Roles and Features**
   * Select **Group Policy Management**
   * Finish installation

#### Step 2:
Open GPMC via:

   ```
   Start > Administrative Tools > Group Policy Management
   ```

---

### 🧪 Creating GPOs + Types of GPOs

There are multiple ways to create and assign GPOs. Below are the steps and types.

#### How to Create a GPO:

1. Open **Group Policy Management**
2. Right-click on the **OU or Domain** where you want to apply the GPO
3. Select **Create a GPO in this domain, and Link it here**
4. Name your GPO (e.g., *PasswordPolicy-GPO*)
5. Right-click the GPO and choose **Edit**
6. Configure settings under **Computer Configuration** or **User Configuration**

--- 

#### Types of GPOs:

| Type            | Description                                                 |
| --------------- | ----------------------------------------------------------- |
| **Local GPO**   | Applies only to local machines                              |
| **Domain GPO**  | Managed centrally via AD DS                                 |
| **Starter GPO** | Template GPO used to create new GPOs with baseline settings |
| **Linked GPO**  | GPOs linked to Sites, Domains, or OUs                       |

---


### 🧩 GPO 1 - Scenario - Enforcing password length

![Project-3-GPO-Management](GP-create-new-1.png "My Project Logo")

![Project-3-GPO-Management](GP-create-new-edit.png "My Project Logo")

Linked to Domain Computers

![Project-3-GPO-Management](GP-create-new-linked.png "My Project Logo")


![Project-3-GPO-Management](GP-create-new-password-settings.png "My Project Logo")

![Project-3-GPO-Management](GP-create-new-verify.png "My Project Logo")

![Project-3-GPO-Management](GP-create-new-verify2.png "My Project Logo")


User Test - Tony Stark - BERTO\tstark

![Project-3-GPO-Management](BERTO-tstark-login.png "My Project Logo")

![Project-3-GPO-Management](BERTO-tstark-password-change-login.png "My Project Logo")

Succesfully encountered error as per GPO password length

![Project-3-GPO-Management](BERTO-tstark-password-change-ERROR.png "My Project Logo")



### 🧩 GPO 2 - Scenario - Preventing access to Control Panel

![Project-3-GPO-Management](GPO-prevent-control-panel-access1.png "My Project Logo")

![Project-3-GPO-Management](GPO-prevent-control-panel-access2.png "My Project Logo")

![Project-3-GPO-Management](GPO-prevent-control-panel-access3.png "My Project Logo")

![Project-3-GPO-Management](GPO-prevent-control-panel-access4.png "My Project Logo")




User Test - Tony Stark - BERTO\tstark



![Project-3-GPO-Management](GPO-control-panel-gpresult.png "My Project Logo")

![Project-3-GPO-Management](GPO-control-panel-gpresult-check.png "My Project Logo")

![Project-3-GPO-Management](GPO-control-panel-gpresult-message.png "My Project Logo")




### 🧩 GPO 3 - Scenario - Prevent user access to Powershell



![Project-3-GPO-Management](GPO-disable-powershell-access1.png "My Project Logo")


![Project-3-GPO-Management](GPO-disable-powershell-access2.png "My Project Logo")


![Project-3-GPO-Management](GPO-disable-powershell-access3.png "My Project Logo")


![Project-3-GPO-Management](GPO-disable-powershell-access-verify.png "My Project Logo")




### Bonus - Create a GPO via Powershell script - All settings disabled


![Project-3-GPO-Management](GPO-PS-disable-wallpaper.png "My Project Logo")



---

### 🧾 Conclusion

This lab highlights my capability to:

* Build and configure a fully functional Windows Server lab environment
* Understand and apply Group Policy to enforce enterprise security controls
* Document and automate configuration management

**It demonstrates my foundational skills in system administration, security policy enforcement, and enterprise IT management.**
