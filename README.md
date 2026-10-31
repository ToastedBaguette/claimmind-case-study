# Case Study: Taking an AI Claims Platform from Code to Hospitals Across Indonesia

**Rony Hartono Irawan** · Software Engineer at ClaimMind
[LinkedIn](https://www.linkedin.com/in/rony-hartono-irawan) · [GitHub](https://github.com/ToastedBaguette)

> ClaimMind is now live at **hospitals across Indonesia**, processing **~66,000 claims a month**.
> The initial check casemix staff do on each inpatient claim dropped from **~15 minutes to ~2**.

---

## The problem

In Indonesian hospitals, casemix staff check every inpatient claim before it is submitted to BPJS. That first check took about 15 minutes per claim, because staff did three things by hand:

1. **Document completeness:** confirm every billed item has its supporting document. A lab charge needs its lab result.
2. **ICD coding:** code the patient's diagnoses into ICD.
3. **Compliance:** check those codes against BPJS references, such as the national clinical guidelines (PNPK).

With thousands of claims a month per hospital, that time adds up fast.

## What we built

ClaimMind is a multi-tenant SaaS platform (Next.js, TypeScript, Keycloak, PostgreSQL) that supports casemix staff through all three steps. It recommends which documents are missing, suggests ICD codes, and checks whether those codes are valid under BPJS references.

The hard part is that every hospital is a little different. BPJS verifiers in different regions have different preferences for what gets a claim pended. So the checks start from national guidelines, and each hospital can customize them.

## My role

- **Engineering:** I own the frontend architecture and take on backend and data work when needed, including SQL reporting and tracing data discrepancies.
- **Rollout:** For our first hospital clients, I led every stage myself: kickoff, user training, go-live, and weekly post-launch meetings.
- **Fitting the hospital's workflow:** I designed parts of the setup around how hospital staff already work, so go-live didn't add confusion.
- **Scaling:** As the client base grew, onboarding moved to a dedicated client engagement engineer. I became the technical escalation point in client meetings and still support new kickoffs and go-lives.

## How I handle client requests

When a hospital asks for something complex, I don't just say yes or no. I explain why it takes time, then offer two paths: a quick solution that unblocks them now, or the proper solution that takes longer but holds up. The client chooses, knowing the tradeoff.

**Example: creating custom rules.** Hospitals can add their own rules on top of the national defaults. In the first version, users filled in many fields by hand for every rule. Users asked us to make it simpler, so we offered two paths:

| | Quick solution | Proper solution |
|---|---|---|
| **How it works** | Users describe a rule in plain words; the system fills in the fields | Users upload the guideline documents they already use; the system generates rules from them |
| **User control** | Users review before saving | Users review every rule before use |

Both are now live. Users pick the approach that fits the task, and no one enters rules field by field anymore.

## What I learned

**Similar problems aren't the same problem.** Hospitals share the same high-level problems, but the details differ when you look closely. A solution built for one hospital rarely fit the next one as it was.

**Design at two levels.** I learned to look for a product-level core that fits current and future hospitals, plus a layer each hospital can customize. That way a new client doesn't need a new custom build.

**Every rollout makes the next one easier.** When a new hospital describes a problem we've already solved, I can tell them how a previous client handled it, which builds trust quickly. Doing the first rollouts by hand is also what made onboarding repeatable enough to hand to a dedicated role.

---

*Details are kept at a high level to protect client and company information. No hospital names or proprietary code are included.*
