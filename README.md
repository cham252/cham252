# Vulnerability Management Program Implementation

In this project, we simulate the implementation of a comprehensive vulnerability management program, from inception to completion.

_**Inception State:**_ the organization has no existing policy or vulnerability management practices in place.

_**Completion State:**_ a formal policy is enacted, stakeholder buy-in is secured, and a full cycle of organization-wide vulnerability remediation is successfully completed.

---

<img width="500" alt="image" src="https://github.com/cham252/Vulnerability-Management-Program/blob/main/Vulnerability%20Image.png">

# Technology Utilized
- Tenable (enterprise vulnerability management platform)
- Azure Virtual Machines (Nessus scan engine + scan targets)
- PowerShell & BASH (remediation scripts)

---


# Table of Contents

- [Vulnerability Management Policy Draft Creation](#vulnerability-management-policy-draft-creation)
- [Mock Meeting: Policy Buy-In (Stakeholders)](#step-2-mock-meeting-policy-buy-in-stakeholders)
- [Policy Finalization and Senior Leadership Sign-Off](#step-3-policy-finalization-and-senior-leadership-sign-off)
- [Mock Meeting: Initial Scan Permission (Server Team)](#step-4-mock-meeting-initial-scan-permission-server-team)
- [Initial Scan of Server Team Assets](#step-5-initial-scan-of-server-team-assets)
- [Vulnerability Assessment and Prioritization](#step-6-vulnerability-assessment-and-prioritization)
- [Distributing Remediations to Remediation Teams](#step-7-distributing-remediations-to-remediation-teams)
- [Mock Meeting: Post-Initial Discovery Scan (Server Team)](#step-8-mock-meeting-post-initial-discovery-scan-server-team)
- [Mock CAB Meeting: Implementing Remediations](#step-9-mock-cab-meeting-implementing-remediations)
- [Remediation Round 1: Outdated Wireshark Removal](#remediation-round-1-outdated-wireshark-removal)
- [Remediation Round 2: Insecure Protocols & Ciphers](#remediation-round-2-insecure-protocols--ciphers)
- [Remediation Round 3: Guest Account Group Membership](#remediation-round-3-guest-account-group-membership)
- [Remediation Round 4: Windows OS Updates](#remediation-round-4-windows-os-updates)
- [First Cycle Remediation Effort Summary](#first-cycle-remediation-effort-summary)

---

### Vulnerability Management Policy Draft Creation

This phase focuses on drafting a Vulnerability Management Policy as a starting point for stakeholder engagement. The initial draft outlines scope, responsibilities, and remediation timelines, and may be adjusted based on feedback from relevant departments to ensure practical implementation before final approval by upper management.  
[Draft Policy](https://docs.google.com/document/d/1CLSWm1_9JL1oUqgyNNwtPXW6FzXJ7ddVnSAUQTyqC8I/edit?usp=drive_link)

---

### Step 2) Mock Meeting: Policy Buy-In (Stakeholders)

In this phase, a meeting with the server team introduces the draft Vulnerability Management Policy and assesses their capability to meet remediation timelines. Feedback leads to adjustments, like extending the critical remediation window from 48 hours to one week, ensuring collaborative implementation.


<img width="500" alt="image" src="https://github.com/cham252/Vulnerability-Management-Program/blob/main/management.jpeg">

<details>
  <summary><strong>Vulnerability Management Policy Discussion (Chris & Tony)</strong></summary>

  <p><strong>Chris:</strong> Good morning, Tony. How’s everything been lately? I know everyone’s been busy these last few weeks.</p>
  <p><strong>Tony:</strong> Good morning, Chris. It’s been a bit hectic, but we’re hanging in there. I read the policy draft and it makes sense. However, with our current staffing levels, we can’t meet the aggressive remediation timelines—especially the 48-hour window for critical vulnerabilities.</p>
  <p><strong>Chris:</strong> I understand. Let’s extend the critical remediation window to <strong>one week</strong> and reserve <strong>48 hours</strong> for truly severe zero-days.</p>
  <p><strong>Tony:</strong> That’s reasonable. Could we also have some leeway as we get used to the process—maybe for the first few months?</p>
  <p><strong>Chris:</strong> Yes. After finalizing the policy, we’ll start the program and give departments <strong>~6 months</strong> to adjust.</p>
  <p><strong>Tony:</strong> Sounds great. Thanks for including us in the decision-making.</p>
  <p><strong>Chris:</strong> We’re all in this together.</p>
  <p><strong>Tony:</strong> Thanks for the short meeting.</p>
  <p><strong>Chris:</strong> My favorite kind. Take care!</p>
  <p><strong>Tony:</strong> See you later.</p>
</details>
    
---
### Step 3) Policy Finalization and Senior Leadership Sign-Off

After gathering feedback from the server team, the policy is revised, addressing aggressive remediation timelines. With final approval from upper management, the policy now guides the program, ensuring compliance and reference for pushback resolution.  
<div align="center">
  <img width="300" alt="Initial Scan Meeting" src="https://github.com/cham252/Vulnerability-Management-Program/blob/main/Meeting%2023%202.png">
</div>
---

### Step 4) Mock Meeting: Initial Scan Permission (Server Team)

The team collaborates with the server team to initiate scheduled credential scans. A compromise is reached to scan a single server first, monitoring resource impact, and using just-in-time Active Directory credentials for secure, controlled access.  
<img width="500" alt="image" src="https://github.com/cham252/Vulnerability-Management-Program/blob/main/Meeting%20%23%202.png">

---

### Step 5) Initial Scan of Server Team Assets

In this phase, an insecure Windows Server is provisioned to simulate the server team's environment. After creating vulnerabilities, an authenticated scan is performed, and the results are exported for future remediation steps.


  <img src="https://raw.githubusercontent.com/cham252/Vulnerability-Management-Program/main/Initial%20Scan.png" 
       alt="Initial Scan of Server Team Assets" 
       width="500" 
       style="border: 2px solid black; border-radius: 10px;">
</p>



---

### Step 6) Vulnerability Assessment and Prioritization

We assessed vulnerabilities and established a remediation prioritization strategy based on ease of remediation and impact. The following priorities were set:

1. Third Party Software Removal (Wireshark)
2. Windows OS Secure Configuration (Protocols & Ciphers)
3. Windows OS Secure Configuration (Guest Account Group Membership)
4. Windows OS Updates

---

### Step 7) Distributing Remediations to Remediation Teams

The server team received remediation scripts and scan reports to address key vulnerabilities. This streamlined their efforts and prepared them for a follow-up review.  

<img width="635" alt="image" src="https://github.com/user-attachments/assets/bbf9478f-e1d1-4898-846e-b510ec8c6f72">

[Remediation Email](https://github.com/joshmadakor1/lognpacific-public/blob/main/misc/remediation-email.md)

---

### Step 8) Mock Meeting: Post-Initial Discovery Scan (Server Team)

The server team reviewed vulnerability scan results, identifying outdated software, insecure accounts, and deprecated protocols. The remediation packages were prepared for submission to the Change Control Board (CAB). 

<img width="500" alt="image" src="https://github.com/cham252/Vulnerability-Management-Program/blob/main/meeting%20%23%203.png">
<details>
  <summary><strong>Post Initial Discovery Scan Discussion (Chris & Tony)</strong></summary>

  <p><strong>Chris:</strong> Morning, Tony. How are you doing?</p>
  <p><strong>Tony:</strong> Not bad for a Monday. How about you?</p>
  <p><strong>Chris:</strong> Still alive, so I can’t complain. Before we dive into the vulnerabilities, how did the scan go on your end? Any outages or overutilization issues?</p>
  <p><strong>Tony:</strong> The scan went well. We monitored the systems, and aside from all the open connections, we wouldn’t have even noticed a scan was taking place.</p>
  <p><strong>Chris:</strong> That’s good news. I expected as much. We’ll keep monitoring, but I don’t anticipate any resource issues. Mind if I go over the vulnerability findings?</p>
  <p><strong>Tony:</strong> Not at all. Go ahead.</p>
  <p><strong>Chris:</strong> Great. So, most of the findings are from Wireshark being installed—it’s just really out of date. One interesting thing: the local guest account on several servers belongs to the local administrators group. I’m not sure why that is.</p>
  <p><strong>Tony:</strong> That’s strange.</p>
  <p><strong>Chris:</strong> Yeah. Also, some vulnerabilities may automatically resolve after Windows updates—like the Microsoft Edge Chromium one. The self-signed certificate alert isn’t a big concern, but the deprecated cipher suites and TLS 1.0/1.1 protocols should be addressed. So basically, we’re looking at removing outdated Wireshark versions, disabling the guest account, and deprecating those old cipher suites.</p>
  <p><strong>Tony:</strong> Makes sense. The good news is that most of our servers probably share the same vulnerabilities, so remediation should be fairly consistent.</p>
  <p><strong>Chris:</strong> Exactly. Do you foresee any issues remediating the cipher suites or protocols?</p>
  <p><strong>Tony:</strong> Not really. We’ll run everything through the next Change Control Board. Uninstalling Wireshark and fixing the guest account should be straightforward. I’ll talk to our sysadmins to confirm.</p>
  <p><strong>Chris:</strong> Perfect. I’ll build out some remediation packages to make the process easier. Do you already have something in place for handling Windows Update–related vulnerabilities?</p>
  <p><strong>Tony:</strong> Yes, our patch management takes care of that automatically—usually within a week.</p>
  <p><strong>Chris:</strong> Excellent. I’ll research the best remediation methods and get back to you before the next Change Control Board.</p>
  <p><strong>Tony:</strong> Sounds good. Talk to you soon.</p>
  <p><strong>Chris:</strong> Cool, talk soon.</p>

</details>

---
### Step 9) Mock CAB Meeting: Implementing Remediations

The Change Control Board (CAB) reviewed and approved the plan to remove insecure protocols and cipher suites. The plan included a rollback script and a tiered deployment approach.  
<img width="500" alt="image" src="https://github.com/cham252/Vulnerability-Management-Program/blob/main/Meeting%20%23%204.png">
<details>
  <summary><strong>CAB Meeting Discussion (Chris & Tony and Team)</strong></summary>

  <p><strong>Moderator:</strong> Next up on the list are a couple of vulnerability remediations for the server team:</p>
  <ul>
    <li>Removal of insecure protocols</li>
    <li>Removal of insecure cipher suites</li>
  </ul>
  <p>It looks like <strong>Chris</strong> from the Risk Department is working with <strong>Tony</strong> from Infrastructure on this. Tony, do you want to walk us through the technical aspects of the change being implemented?</p>

  <p><strong>Tony:</strong> Normally, I would, but could I give this one to Chris? He actually built the solution for us—we’re still getting used to the process.</p>

  <p><strong>Chris:</strong> Sure thing. Basically, insecure cipher suites and protocols are older or deprecated algorithms that can still be used if left enabled. That means if a system connects to a server that only supports those insecure protocols, it could negotiate and use them.</p>

  <p>These configurations are controlled through the Windows Registry. The fix is straightforward—we wrote a PowerShell script that disables all insecure protocols and ciphers, and then enables only the secure, standardized ones used today.</p>

  <p><strong>Moderator:</strong> That sounds good, but what if something goes wrong? Do we have a rollback plan in place?</p>

  <p><strong>Chris:</strong> Absolutely. We’ve set up a <strong>tiered deployment</strong> approach—starting with a pilot group, then pre-production, and finally full production rollout. On top of that, we built automated rollback scripts that can restore the original registry settings if any issues arise.</p>

  <p><strong>Moderator:</strong> Excellent. Since the fixes are simple registry updates, I’m not too concerned. Any other questions from the team?</p>

  <p><strong>Team:</strong> None here.</p>

  <p><strong>Moderator:</strong> Great. That wraps up this week’s CAB meeting. See you all next week.</p>

  <p><strong>Chris & Tony:</strong> See you later.</p>

</details>

---
### Step 10 ) Remediation Effort

#### Remediation Round 1: Outdated Wireshark Removal

The server team used a PowerShell script to remove outdated Wireshark. A follow-up scan confirmed successful remediation.  
[Wireshark Removal Script](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/remediation-wireshark-uninstall.ps1)  

<p align="center">
  <img src="https://raw.githubusercontent.com/cham252/Vulnerability-Management-Program/main/Scan2.png" alt="Scan 2 Results" width="650" style="border: 2px solid black; border-radius: 10px;">
</p>

[Scan 2 - Third Party Software Removal](https://drive.google.com/file/d/1UiwPPTtuSZKk02hiMyXf31pXUIeC5EWt/view?usp=drive_link)


#### Remediation Round 2: Insecure Protocols & Ciphers

The server team used PowerShell scripts to remediate insecure protocols and cipher suites. A follow-up scan verified successful remediation, and the results were saved for reference.

[PowerShell: Insecure Protocols Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-protocols.ps1)  
<p align="center">
  <img src="https://raw.githubusercontent.com/cham252/Vulnerability-Management-Program/main/Scan3.png" alt="Remediation Scan 3 - Insecure Protocols and Ciphers" width="650" style="border: 2px solid black; border-radius: 10px;">
</p>
[Scan 3 - Ciphersuites and Protocols](https://drive.google.com/file/d/1Qc6-ezQvwReCGUZNtnva0kCZo_-zW-Sm/view?usp=drive_link)


#### Remediation Round 3: Guest Account Group Membership

The server team removed the guest account from the administrator group. A new scan confirmed remediation, and the results were exported for comparison.

[PowerShell: Guest Account Group Membership Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-guest-local-administrators.ps1)

<p align="center">
  <img src="https://raw.githubusercontent.com/cham252/Vulnerability-Management-Program/main/Scan4.png" 
       alt="Remediation Scan 4 - Guest Account Group Membership" 
       width="650" 
       style="border: 2px solid black; border-radius: 10px;">
</p>

[Scan 4 - Guest Account Group Removal](https://drive.google.com/file/d/1jVgkjjfrV1YjOcL3QRT_oUB0Y82w22V7/view?usp=drive_link)


#### Remediation Round 4: Windows OS Updates

Windows updates were re-enabled and applied until the system was fully up to date. A final scan verified the changes.

<p align="center">
  <img src="https://raw.githubusercontent.com/cham252/Vulnerability-Management-Program/main/Scan5.png" 
       alt="Remediation Scan 5 - Windows OS Updates" 
       width="650" 
       style="border: 2px solid black; border-radius: 10px;">
</p>

[Scan 5 - Post Windows Updates](https://drive.google.com/file/d/1tmDjeH15uiGitRwvWy8kFRi33q-nGi1Zt/view?usp=drive_link)
---

### First Cycle Remediation Effort Summary

The remediation process reduced total vulnerabilities by 76%, from 26 to 6. Critical vulnerabilities were resolved by the second scan (100%), and high vulnerabilities dropped by 90%. Mediums were reduced by 76%. In an actual production environment, asset criticality would further guide future remediation efforts.  

<img width="1920" alt="image" src="https://github.com/user-attachments/assets/51f0aae8-7f36-4d90-b29f-5257e57155f9">

[Remediation Data](https://docs.google.com/spreadsheets/d/1FTtFfZYmFsNLU6pm8nTzsKyKE-d2ftXzX_DPwcnFNfA/edit?gid=0#gid=0)

---

### On-going Vulnerability Management (Maintenance Mode)

After completing the initial remediation cycle, the vulnerability management program transitions into **Maintenance Mode**. This phase ensures that vulnerabilities continue to be managed proactively, keeping systems secure over time. Regular scans, continuous monitoring, and timely remediation are crucial components of this phase. (See [Finalized Policy](https://docs.google.com/document/d/1rvueLX_71pOR8ldN9zVW9r_zLzDQxVsnSUtNar8ftdg/edit?usp=drive_link) for scanning and remediation cadence requirements.)

Key activities in Maintenance Mode include:
- **Scheduled Vulnerability Scans**: Perform regular scans (e.g., weekly or monthly) to detect new vulnerabilities as systems evolve.
- **Patch Management**: Continuously apply security patches and updates, ensuring no critical vulnerabilities remain unpatched.
- **Remediation Follow-ups**: Address newly identified vulnerabilities promptly, prioritizing based on risk and impact.
- **Policy Review and Updates**: Periodically review the Vulnerability Management Policy to ensure it aligns with the latest security best practices and organizational needs.
- **Audit and Compliance**: Conduct internal audits to ensure compliance with the vulnerability management policy and external regulations.
- **Ongoing Communication with Stakeholders**: Maintain open communication with teams responsible for remediation, ensuring efficient coordination.

By maintaining an active vulnerability management process, organizations can stay ahead of emerging threats and ensure long-term security resilience.
