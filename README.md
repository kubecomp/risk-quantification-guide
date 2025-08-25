
## 1. Scoring Model
- **Likelihood (1–5)**: 1 = Rare, 5 = Almost Certain
- **Impact (1–5)**: 1 = Negligible, 5 = Severe / Business-crippling
- **Risk Score = Likelihood x Impact**

| Score | Level      | Action                                |
|-------|------------|---------------------------------------|
| 1–5   | Low        | Accept / monitor                      |
| 6–10  | Medium     | Mitigate with planned controls        |
| 11–15 | High       | Immediate treatment, exec visibility  |
| 16–25 | Critical   | Escalate to Board; urgent mitigation  |

## 2. Example: Executive Summary
> **Top Risks – Q3 2025**
> - **Unauthorized access to production (Score: 20 – Critical)**  
>   Controls: MFA, SSO, IAM reviews. Residual: 8 (Medium).  
> - **Vendor data breach (Score: 15 – High)**  
>   Controls: TPRM, DPAs, SOC 2 reviews. Residual: 9 (Medium).  
> - **Unpatched critical vulnerabilities (Score: 16 – Critical)**  
>   Controls: Weekly scanning, SLA remediation. Residual: 6 (Medium).  

📊 **Trend**: Critical risks reduced from 4 → 2 since Q2 due to IAM improvements.  

---

## 📂 Repo: `security-policies`
**File:** `iam-access-review-checklist.md`  
**Commit message:** `Add IAM access review checklist with quarterly review steps`

```markdown
# IAM Access Review Checklist

## Frequency
- Quarterly for critical apps and infrastructure
- Semi-annual for lower-risk systems

## Steps
1. **Pull access list** from IAM tool, SSO, or system exports  
2. **Validate role alignment** – each user has least-privilege role  
3. **Check joiner/mover/leaver events** – confirm timely provisioning/deprovisioning  
4. **Flag orphaned accounts** – disable or remediate immediately  
5. **Service accounts** – validate justification, vaulting, and rotation  
6. **Document findings** – approvals, revocations, risk acceptance  
7. **Report metrics** – % of accounts reviewed, # of removals, exceptions  

✅ Use evidence (tickets, signed review logs, system screenshots) for audits.
