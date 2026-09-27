<h1 align="center">Microsoft Intune (Endpoint Management & MDM)</h1>

This repository demonstrates modern Mobile Device Management (MDM) and Mobile Application Management (MAM) using Microsoft Intune. The lab focuses on cloud-based device enrollment, compliance policies, configuration profiles, and remote Help Desk troubleshooting.


### Cross-Platform Device Enrollment (Windows & Android)

To establish cloud-based management and simulate a modern BYOD (Bring Your Own Device) environment, both a Windows virtual machine and an Android mobile device were enrolled into Microsoft Intune. The Windows endpoint was joined directly to Entra ID, while the Android device was provisioned with a secure corporate Work Profile via the Managed Google Play connector. 

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/c5988438-4dcb-425f-97f0-3c364577f5c9" />

### Security Compliance Policies

To enforce organizational security baselines, a Compliance Policy was deployed via Intune. The policy requires all managed Windows endpoints to have active firewalls, antivirus protection, and real-time threat monitoring enabled. Devices failing to meet these criteria are flagged as non-compliant, which can conditionally restrict their access to corporate resources.

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/a9291bd3-fe2f-4d78-9d87-616fe0c099bf" />

### Configuration Profiles (Device Restrictions)

To mitigate unauthorized hardware usage and harden the endpoint, a Configuration Profile was deployed to managed Windows devices. A Device Restriction policy was configured to explicitly block access to specific local hardware features, simulating standard enterprise endpoint security measures.

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/8481a86b-6090-42eb-8f86-d04d729be910" />

### Cloud Application Deployment

To streamline user onboarding and ensure standardized software availability, corporate applications were deployed silently via Intune. Microsoft 365 Apps were pushed directly to the managed endpoints over the cloud, eliminating the need for manual installations or local administrative privileges.

<img width="1364" height="767" alt="image" src="https://github.com/user-attachments/assets/a3e2e47c-c089-4d84-8b7c-862492e7fb6a" />
<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/9068aa3f-fc34-4438-a981-da39860d512d" />
<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/b2809fad-1143-4b96-b8c4-fe1ca06caff4" /> 
<img width="250" alt="Screenshot_20260926_225321_One UI Home" src="https://github.com/user-attachments/assets/f61e9161-21a6-4f51-8483-f4d07d60c97e" />

### Endpoint Security (BitLocker Encryption)

To ensure data at rest remains secure, a BitLocker encryption profile was deployed via Intune's Endpoint Security blade. The policy mandates silent, full-disk encryption on managed Windows endpoints and automatically escrows the BitLocker Recovery Keys directly into Microsoft Entra ID for secure Help Desk retrieval.

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/e198491e-4c00-4b40-a808-44c703abaa0c" />

### Remote Script Execution (PowerShell)

To automate administrative tasks and provision local resources, custom PowerShell scripts were deployed via Intune. This demonstrates the ability to execute background configurations, modify local filesystems, and manage endpoints at scale without disrupting the end-user experience.

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/f198caf1-6033-4584-941e-b03f5a5683d7" />

### Remote Help Desk Management & Device Wipe

To simulate a lost or stolen device scenario, remote Help Desk actions were executed directly from the cloud console. A remote device wipe was initiated to securely erase corporate data and factory reset the endpoint, ensuring data loss prevention (DLP) without requiring physical access to the machine.

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/d4b9bc96-b807-42cd-9bca-a11509ea2ba8" />
