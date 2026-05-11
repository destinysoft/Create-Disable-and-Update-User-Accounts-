#  User Account Creation and Management

> **Author:** Destiny Osamudiamen
> 
> **Domain:** Active Directory Administration
> 
> **Environment:** Windows Server 2022 + Windows 11 Client Virtual Lab ( VMware Workstation Pro )  
> **Completed:** May 2026

---

## Objective

Create a new domain user account inside a dedicated Organisational Unit, populate all relevant profile attributes, assign the account to an appropriate security group, disable the account in response to an HR suspension request and then re-enable it when access is reinstated.

---

## Business Scenario

> **Ticket #0011 | New Starter Provisioning + Temporary Suspension**
>
> HR has submitted a new starter request for **Bob Thornton**, joining the Sales department as a Sales Assistant. The account needs to be created, fully populated with contact and organisational details and added to the Sales security group before their start date.
>
> A follow-up request arrives shortly after: HR asks for access to be suspended temporarily while an onboarding matter is resolved. Once cleared, they request the account be reinstated.

This scenario covers two of the most routine tasks in any IT support role which is provisioning a new account and managing the user lifecycle through disable and re-enable actions.

---

## Environment and Tools Used

| Component | Detail |
|---|---|
| **Server OS** | Windows Server 2022 Evaluation |
| **Domain** | mylab.local |
| **Tool** | Active Directory Users and Computers (ADUC) |
| **Access path** | Server Manager → Tools → ADUC |
| **User created** | Bob Thornton (Bton@mylab.local) |
| **OU created** | Office Users |
| **Group created** | Sales (Global Security) |

---

## Lab Architecture

```
mylab.local
│
├── Builtin
├── Computers
├── Domain Controllers
├── Users
│     └── (default domain users)
│
└── Office Users          ← OU created in this lab
      ├── Bob Thornton     ← User created in this lab
      └── Sales           ← Security group created in this lab
```

---

## Steps Performed

---

### Phase 1 - Access Active Directory Users and Computers

**Step 1.1 - Open Server Manager**

Press the `Windows` key, type **Server Manager**, and open it. This is the central administration console on Windows Server from which all AD tools are accessed.




---

**Step 1.2 - Navigate to ADUC via Tools Menu**

Inside Server Manager, click **Tools** in the top-right menu bar and select **Active Directory Users and Computers** from the dropdown list.


