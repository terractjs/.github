# Terract Code of Conduct

> The Terract community is built on trust. Every rule here exists to protect that trust — for users, developers, and contributors alike. This document is not a formality. It is the foundation of everything we build together.

---

## Table of Contents

1. [Our Pledge](#our-pledge)
2. [Our Values](#our-values)
3. [Community Standards](#community-standards)
4. [Package & App Requirements](#package--app-requirements)
5. [The Verification System](#the-verification-system)
6. [How Verification Works](#how-verification-works)
7. [Closed Source Policy](#closed-source-policy)
8. [User Data & Privacy Rules](#user-data--privacy-rules)
9. [Terract Shield Compliance](#terract-shield-compliance)
10. [The Ruling System](#the-ruling-system)
11. [Reporting a Violation](#reporting-a-violation)
12. [Enforcement Process](#enforcement-process)
13. [Appeals](#appeals)
14. [Maintainer Commitments](#maintainer-commitments)
15. [Scope](#scope)

---

## Our Pledge

We as members, contributors, maintainers, and users of the Terract ecosystem pledge to make participation in our community a safe, respectful, and harassment-free experience for everyone.

This pledge extends to every person regardless of age, body size, disability, ethnicity, sex characteristics, gender identity and expression, level of experience, education, socio-economic status, nationality, personal appearance, race, caste, color, religion, or sexual identity and orientation.

We pledge to act and interact in ways that contribute to an open, welcoming, diverse, inclusive, and healthy community — and to hold ourselves and each other accountable when we fall short.

User safety is not a feature. It is a requirement. It comes before everything else.

---

## Our Values

These are the core values that drive every decision in the Terract ecosystem:

**Trust** — Every user who installs a Terract-based app trusts us. We do not take that lightly. We protect it above all else.

**Transparency** — We do not hide how things work. Not the framework. Not the verification process. Not enforcement decisions. Everything is documented and visible.

**Accountability** — Mistakes happen. What matters is owning them, fixing them, and learning from them. We hold ourselves to this standard and expect the same from our community.

**Safety First** — Before performance, before features, before anything — the safety of the user comes first. This is non-negotiable.

**Inclusivity** — Anyone can use Terract. Anyone can contribute. Nobody gets gatekept based on who they are.

**Quality** — We care deeply about what gets published under the Terract name. Low-quality, deceptive, or harmful packages damage everyone.

---

## Community Standards

### What We Expect

- Communicate with kindness, patience, and respect at all times
- Welcome newcomers and help them get started
- Give constructive, honest feedback — not harsh or dismissive criticism
- Accept feedback gracefully and use it to improve
- Take responsibility for your actions and their impact on others
- Put the community's wellbeing above your personal preferences
- Follow all publishing, verification, and compliance requirements
- Report violations when you see them — silence enables harm
- Respect maintainers' time and decisions even when you disagree

### What We Do Not Tolerate

- Harassment, bullying, or intimidation of any kind — public or private
- Discrimination based on any personal characteristic
- Sexualized language, imagery, or behavior in any community space
- Deliberate misgendering or use of rejected names
- Publishing apps or packages that violate user privacy
- Bypassing or attempting to circumvent Terract Shield
- Distributing malicious, deceptive, or harmful packages
- Spamming community channels, issues, or pull requests
- Impersonating other developers, maintainers, or official Terract accounts
- Sharing private information of others without explicit consent
- Trolling, derailing conversations, or bad-faith arguments
- Retaliating against anyone who makes a report
- Threatening or intimidating maintainers or contributors
- Any behavior that a reasonable person would consider inappropriate in a professional setting

---

## Package & App Requirements

Every package, plugin, component, or application published within the Terract ecosystem must meet all of the following requirements without exception.

### 1. Permission Compliance

Your app must never bypass, work around, or suppress Terract Shield. Every access to the file system, network, environment variables, clipboard, or any other system resource must go through Terract's permission prompt. The user must be informed and must consent before any access occurs.

This rule applies even if the developer forgot to implement it. Terract Shield is enforced at the framework level. Any attempt to override or disable it at the package level is a critical violation.

### 2. Honest & Accurate Descriptions

Your package name, description, README, and all documentation must accurately and honestly represent what your app does. If your app's behavior changes in a future version, your documentation must be updated to reflect that before or alongside the release.

Misleading descriptions — intentional or not — will result in immediate removal until corrected.

### 3. No Malicious Code

Your package must not contain any of the following:

- Malware or ransomware of any kind
- Spyware or stalkerware
- Cryptominers or resource hijackers
- Code designed to exploit, deceive, or harm the user
- Hidden network requests not disclosed to the user
- Backdoors or remote access tools not explicitly declared

Packages found to contain malicious code will be removed immediately and the developer permanently banned. Serious cases will be reported to relevant authorities.

### 4. No Unauthorized Data Collection

If your app collects, stores, transmits, or processes any user data you must:

- Declare this explicitly in your package description and README
- Request permission from the user via Terract Shield before any data is collected
- Provide a clear and accessible privacy policy
- Give the user the ability to opt out at any time

Collecting user data without these steps is a serious violation regardless of the type or volume of data collected.

### 5. Open Source by Default

All packages published in the Terract ecosystem must be open source unless the developer has completed and passed the Terract Closed Source Verification process. See the [Closed Source Policy](#closed-source-policy) for full details.

Unverified closed-source packages discovered in the ecosystem will be removed without warning.

### 6. No Impersonation

You may not publish packages that impersonate official Terract packages, use branding designed to confuse users into thinking they are from Terract, or imitate other well-known developers or projects without explicit permission.

### 7. Dependency Responsibility

You are responsible for the dependencies your package uses. If a dependency you rely on is found to be malicious or non-compliant, you are expected to remove or replace it promptly. Ignorance of a dependency's behavior is not an acceptable defense.

### 8. Version Integrity

Every version you publish must be stable, intentional, and documented. Do not publish broken, incomplete, or test builds to production versions. Use pre-release tags for anything that is not production-ready.

---

## The Verification System

The Terract Verification System exists to create a layer of trust between developers and users. A verified developer is one whose work has been reviewed by the Terract team and found to be compliant, safe, and of good quality.

### What Verification Means

- Your GitHub profile and repository have been reviewed by the Terract team
- Your package has been checked for compliance with this Code of Conduct
- Your code has been examined for malicious patterns, privacy violations, and permission bypasses
- You have been found to be acting in good faith

A **Terract Verified** badge will appear next to your repository when installed via Terract. Users can trust that verified packages have passed our review.

### What Verification Does Not Mean

Verification is not a guarantee that a package is perfect or bug-free. It means the package was compliant and safe at the time of review. Developers remain responsible for maintaining compliance after verification.

### Verification Tiers

**Standard Verification** — For new developers. Full review of your repository, code, description, and compliance. Takes up to 7 days.

**Trusted Developer Status** — Earned after maintaining a clean record across multiple verified packages and sustained community contribution. Future packages go through an expedited lightweight review. Takes up to 48 hours.

**Terract Partner** — Reserved for organizations and developers who contribute significantly to the Terract ecosystem. By invitation only.

---

## How Verification Works

We believe in full transparency. Here is exactly how the verification process works, step by step. Nothing is hidden.

### Step 1 — Submission

Open a verification request issue in the `.github` repository using the **Verification Request** issue template. Your submission must include:

- Your GitHub username
- The repository you want verified
- A short description of what your package does
- Confirmation that you have read and agree to this Code of Conduct
- Whether your package is open or closed source

### Step 2 — Initial Triage

Within 48 hours a Terract team member will acknowledge your request and assign it for review. If your submission is missing required information you will be asked to provide it before review begins.

### Step 3 — Code Review

A Terract team member will review your repository in full. We check the following:

- Does the package do what it says it does?
- Does it use Terract Shield correctly for all system access?
- Does it collect any user data? If so, is it declared and permissioned correctly?
- Are there any suspicious network requests, hidden behaviors, or obfuscated code?
- Are dependencies reputable and non-malicious?
- Is the README honest and accurate?
- Is the package open source or has closed source verification been completed?
- Is the code of reasonable quality and not dangerously written?

### Step 4 — Decision

After review, one of three outcomes will be issued:

**Approved** — Your package is verified. The Terract Verified badge is applied. You will be notified via your GitHub issue and the badge will appear within 24 hours.

**Approved with Requests** — Your package is mostly compliant but requires minor changes before verification is finalized. You will be given clear instructions on what to fix and a reasonable timeframe to do so. Once changes are made, verification completes without a full re-review.

**Rejected** — Your package does not meet our standards. You will be told exactly why. You may resubmit after addressing all issues. Rejection is not permanent unless it involves malicious intent.

### Step 5 — Ongoing Compliance

Verification is not a one-time event. We conduct periodic re-reviews of verified packages — especially when major updates are published. If a verified package is found to have become non-compliant after verification, the badge will be revoked and the developer notified with a clear explanation and correction path.

### Step 6 — Trusted Developer Upgrade

After maintaining a clean verified record across 3 or more packages over a sustained period, you may be automatically upgraded to Trusted Developer Status or you may request the upgrade manually. The Terract team will review your full history before granting this status.

---

## Closed Source Policy

We believe open source is the foundation of trust. However, we recognize that some developers have legitimate reasons for keeping their source private. Terract supports this — with conditions.

### Applying for Closed Source Verification

To publish a closed-source package in the Terract ecosystem you must complete the Closed Source Verification process in addition to standard verification. This involves:

- Submitting your package binary and build artifacts for review
- Providing a detailed written description of every system access and network request your app makes
- Signing the Terract Closed Source Agreement — a binding commitment to comply with this Code of Conduct
- Agreeing to periodic audits where you provide updated build artifacts for re-review

### Closed Source Restrictions

Closed source packages in the Terract ecosystem are subject to additional restrictions:

- You must provide a public changelog with every release
- You must respond to security disclosures within 72 hours
- You must notify the Terract team of any major behavioral changes before publishing
- You may not obfuscate code in a way that makes security review impossible

Failure to comply with any of these restrictions will result in immediate removal and revocation of closed source verification.

---

## User Data & Privacy Rules

User data is sacred. These rules exist to protect the people who use apps built on Terract.

- Never collect data the user has not explicitly consented to
- Never sell, share, or transfer user data to third parties without explicit consent
- Never store sensitive data — passwords, tokens, keys — in plain text
- Always give users the ability to delete their data
- Always be honest about what data you collect and why
- If you experience a data breach, you must notify affected users and the Terract team within 24 hours

---

## Terract Shield Compliance

Terract Shield is our framework-level permission system. It intercepts every attempt to access system resources and prompts the user for consent. This is a core pillar of Terract's security model and it is non-negotiable.

### What Shield Covers

- File system read and write access
- Network requests and WebSocket connections
- Environment variable access
- Clipboard read and write
- Process spawning
- Any other system-level resource access

### Shield Compliance Rules

- You must never attempt to disable, bypass, or override Terract Shield
- You must declare all required permissions in your package manifest before runtime
- You must not request permissions you do not need
- You must not request permissions in bulk when individual permissions would suffice
- Permissions must be requested at the moment they are needed — not all upfront at launch

Any package found to be bypassing Shield will be removed immediately and the developer permanently banned.

---

## The Ruling System

When a violation occurs, the Terract team follows a structured ruling process. Every decision is documented internally and the outcome is communicated to all involved parties. Nothing is arbitrary.

### Violation Levels

---

**Level 1 — Minor**

First-time, low-impact violations. Examples: incorrect package description, missing documentation update, minor community conduct breach.

Action: Written warning. The developer is informed of the issue and given guidance to correct it. No public record. Correction period: 7 days.

---

**Level 2 — Moderate**

Repeated minor violations or a first-time moderate violation. Examples: repeated misleading descriptions after a warning, disrespectful behavior toward community members, non-compliant dependency usage.

Action: Formal warning with a documented internal record. A correction period of 14 days is issued. Failure to comply within the correction period automatically escalates to Level 3.

---

**Level 3 — Serious**

Significant violations that harm the community or ecosystem. Examples: unauthorized data collection, Shield non-compliance, impersonation, harassment, publishing unverified closed-source packages.

Action: Temporary suspension from the Terract ecosystem and all community spaces. All affected packages removed. Verification revoked. Duration: 30 to 90 days depending on severity. Developer must reapply for verification after suspension ends and must demonstrate corrective action.

---

**Level 4 — Critical**

Severe violations that directly harm users or the integrity of the ecosystem. Examples: malicious packages, spyware, data breaches caused by negligence or intent, sustained harassment campaigns.

Action: Permanent ban from the Terract ecosystem and all community spaces. All packages removed permanently. Verification permanently revoked. Serious cases will be escalated and reported to relevant authorities.

---

**Level 5 — Emergency**

Active, ongoing harm to users. Examples: actively distributed malware, live data exfiltration, active exploitation of users in real time.

Action: Immediate removal of all packages without prior notice. Immediate permanent ban. Immediate escalation to relevant authorities. A public security notice will be issued to warn affected users as quickly as possible.

---

### Ruling Principles

- Every ruling is made by at least two Terract team members
- No ruling is made based on a single unverified report
- The accused party is informed and given the opportunity to respond before a final decision — except in Level 5 emergencies where immediate action is required to protect users
- All rulings are documented internally with full reasoning recorded
- Rulings are communicated privately to all involved parties
- Patterns of behavior are considered — a history of minor violations will be treated more seriously than a single isolated incident
- No team member may rule on a case where they have a personal conflict of interest

---

## Reporting a Violation

If you witness or experience a violation of this Code of Conduct, we want to hear from you. Reports are taken seriously, handled with care, and never ignored.

### How to Report

- **GitHub** — Open a private issue in the `.github` repository using the **Violation Report** issue template
- **Discord** — Send a direct message to any Terract team member or use the `#report` channel
- **Email** — Contact us directly at conduct@terract.dev

### What to Include

- A description of what happened
- When and where it occurred
- Any evidence — screenshots, links, logs, package names
- Your GitHub username or Discord handle so we can follow up with you

### Confidentiality

All reports are handled confidentially. The identity of the reporter will not be shared with the accused party without the reporter's explicit consent. Retaliation against anyone who makes a good-faith report is treated as a Level 3 violation at minimum.

---

## Enforcement Process

When a report is received the following process is followed without exception:

1. **Acknowledgement** — The report is acknowledged within 24 hours
2. **Assessment** — The Terract team reviews the report and determines its validity and severity level
3. **Response** — The accused party is notified and given the opportunity to respond — except in Level 5 emergencies
4. **Decision** — At least two team members agree on the ruling and document their reasoning
5. **Action** — The ruling is applied and communicated to all parties privately
6. **Documentation** — The case is documented internally for future reference and pattern tracking

The entire process from report to decision takes no longer than 7 days for standard cases. Emergency cases are handled immediately.

---

## Appeals

If you believe a ruling against you was made in error or without sufficient evidence, you may appeal within 14 days of receiving your ruling.

### How to Appeal

Open an appeal issue in the `.github` repository or contact the team directly. Your appeal must include:

- The original ruling you are appealing
- Your reasoning for why the ruling was incorrect
- Any new evidence or context not previously considered

### Appeal Review

Appeals are reviewed by a different set of team members than those who made the original ruling to ensure impartiality. The appeal decision is final. Appeals submitted after the 14-day window will not be considered unless extraordinary circumstances are demonstrated.

---

## Maintainer Commitments

The Terract team commits to the following:

- Enforcing this Code of Conduct fairly, consistently, and without favoritism
- Reviewing all reports seriously and promptly
- Communicating clearly with all parties involved in a ruling
- Being transparent about enforcement decisions where possible
- Never using enforcement as a tool for personal agendas
- Holding ourselves to the same standards we hold the community to
- Continuously reviewing and improving these standards as the community grows
- Publishing an anonymized enforcement transparency report periodically so the community can see that these rules are actually enforced

---

## Scope

This Code of Conduct applies to all Terract spaces including all repositories in the terractjs GitHub organization, the Terract Discord server, all packages and apps published in the Terract ecosystem, and any public space where an individual is officially representing Terract. It applies to all community members, contributors, maintainers, and anyone who interacts with the Terract ecosystem in any capacity.

---

## Changes to This Document

This Code of Conduct may be updated over time as the community grows. All changes will be announced in the Discord server and documented in the changelog of this repository. Major changes will include a community comment period before taking effect.

---

<p align="center">
  <sub>Terract — Just a terminal framework. Built with trust. Protected by principle.</sub>
</p>
