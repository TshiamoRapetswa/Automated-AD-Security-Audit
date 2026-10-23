
# Automated Active Directory Security Auditing

**PowerShell | Active Directory | Identity Security | Security Reporting**

## Project Overview

The Automated Active Directory Security Auditing project is a PowerShell-based tool designed to assess Active Directory security posture by identifying common identity misconfigurations and potential security exposures.

The `Invoke-ADAudit.ps1` script automates security checks that would otherwise require manual investigation, helping administrators and security analysts identify accounts and configurations that may require remediation.

## What It Does

The tool audits Active Directory for:

- **Password Hygiene:** Identifies enabled accounts configured with non-expiring passwords.
- **Inactive Accounts:** Flags enabled user accounts with no recorded logon activity for more than 90 days.
- **Privileged Access:** Enumerates membership in sensitive administrative groups, including nested group memberships.
- **AS-REP Roasting Exposure:** Detects enabled accounts configured without Kerberos pre-authentication.
- **Kerberoasting Exposure:** Identifies enabled user accounts configured with Service Principal Names (SPNs).

Audit findings are presented in an HTML security dashboard, with CSV export available for further analysis and reporting.

## Project Achievements

- Automated multiple Active Directory security checks through a single PowerShell script.
- Consolidated identity and Kerberos exposure findings into a structured auditing workflow.
- Developed an HTML dashboard concept for reviewing key security metrics and findings.
- Established a lab-based verification approach using test accounts and configurable security scenarios.
- Documented scheduled execution, troubleshooting, and remediation procedures.

## Security Considerations

- Run audits only in environments where you have explicit authorization.
- Use least-privileged accounts with the permissions required for auditing.
- Protect generated reports because they may contain sensitive account and privilege information.
- Validate findings before making changes to production Active Directory.
- Perform testing and remediation exercises in an isolated lab environment whenever possible.
- Never store real credentials or sensitive production data in the repository.

## Disclaimer

This project is intended for educational purposes, authorized security assessments, and defensive Active Directory administration. Findings indicate potential security exposures and should be validated in context. The tool does not guarantee the detection of every vulnerability or confirm that an account has been compromised.

