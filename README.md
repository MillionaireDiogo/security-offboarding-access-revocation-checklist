# 🔐 Secure Offboarding Checklist

**Purpose:**  
Ensure secure and compliant offboarding of employees, contractors, and third-party users by revoking all access and recovering assets.

---

## ✅ Employee & Contractor Offboarding

### 1. Initiate Offboarding
- [ ] Confirm offboarding date with HR or team lead
- [ ] Notify IT/security team of user separation
- [ ] Inventory user’s accounts, access, and devices

### 2. Revoke Digital Access
- [ ] Disable user in Identity Provider (e.g., Azure AD, Okta, Google Workspace)
- [ ] Remove user from internal and external SaaS platforms (e.g., GitHub, Slack, Jira, Zoom, AWS Console)
- [ ] Invalidate sessions and refresh tokens (SSO, OAuth)
- [ ] Revoke SSH keys, API tokens, and VPN credentials
- [ ] Reset shared credentials (password vaults, shared logins)
- [ ] Reassign or remove MFA/2FA (authenticator apps, hardware tokens)
- [ ] Remove from MDM (e.g., Intune, JAMF)

### 3. Recover Assets
- [ ] Collect company-owned laptops, phones, USBs, security keys
- [ ] Recover ID cards, badges, and physical tokens
- [ ] Wipe and reimage recovered devices

### 4. Transfer Ownership
- [ ] Reassign ownership of email inbox, documents, and project boards
- [ ] Auto-forward emails for a set grace period (if policy allows)
- [ ] Backup user data before deletion

### 5. Compliance & Logging
- [ ] Log all deprovisioning steps (for audit)
- [ ] Notify HR and legal of completion
- [ ] Store logs and records per data retention policy

---

## 🔄 Third-Party / Vendor Offboarding

### 1. Identification
- [ ] Confirm vendor’s last day of service or contract expiration
- [ ] Identify systems, tools, and data they had access to
- [ ] Validate all integrations, IP whitelisting, or firewall rules

### 2. Revoke Access
- [ ] Disable any user accounts created for vendor in internal systems
- [ ] Remove from communication tools (Slack, MS Teams)
- [ ] Remove VPN, firewall, or IP-based access
- [ ] Revoke any issued certificates, API keys, or tokens
- [ ] Review and terminate any automation/scripts deployed by the vendor

### 3. Data & Asset Recovery
- [ ] Request return or deletion of any confidential data
- [ ] Reclaim any hardware, dongles, or test accounts if issued
- [ ] Audit logs for data export/download before exit

### 4. Legal & Compliance
- [ ] Confirm NDAs or data agreements are still in force
- [ ] Document and archive exit steps
- [ ] Perform final security risk review

---

## 📋 Offboarding Tracking Table

| Step                     | Description                                      | Owner            | Status    | Notes         |
|--------------------------|--------------------------------------------------|------------------|-----------|---------------|
| Confirm exit             | With HR/manager or vendor POC                   | HR / Procurement | [ ]       |               |
| Revoke system access     | Identity provider, apps, VPN                    | Security / IT    | [ ]       |               |
| Reset shared credentials | Passwords, vaults                               | Security / DevOps| [ ]       |               |
| Recover devices/assets   | Laptops, tokens, ID cards                        | Admin / HR       | [ ]       |               |
| Transfer data ownership  | Email, docs, repos                              | Team Lead        | [ ]       |               |
| Log deprovisioning       | Ensure audit trail is complete                  | Security         | [ ]       |               |
| Archive records          | Store deprovisioning logs                       | Compliance        | [ ]       |               |

---

## ✨ Automation Tools (Optional)
- **Okta Workflows / Microsoft Entra** – Automate access revocation
- **Terraform / Ansible** – Automate infrastructure-level cleanup
- **Vault / Bitwarden** – Rotate shared credentials
- **SIEM / SOAR tools** – Log, alert, and automate deprovisioning workflows

---

## 🚀 Get Started

To replicate this in your own org or team:

1. Fork this repo
2. Enable issues (if disabled)
3. Use the button below to start tracking offboarding for your team

[👤 Start Employee Offboarding](https://github.com/MzPrincesa/security-offboarding-access-revocation-checklist/blob/e8155307cab042bf66da3947fa2e1fd8392c1820/.github/ISSUE_TEMPLATE/employee-offboarding.yml)

[🏢 Start Vendor Offboarding](https://github.com/MzPrincesa/security-offboarding-access-revocation-checklist/blob/e8155307cab042bf66da3947fa2e1fd8392c1820/.github/ISSUE_TEMPLATE/vendor-offboarding.yml)


> This will launch the interactive checklist using the built-in issue template.

---
