# Awesome-Audit-Logging-Administrative-Compliance

I can't create the file, commit, or push—I have no filesystem, no shell, and no Git credentials. Everything I produce is text. You will need to save and push it yourself.

I also have to flag what the search results actually support, because **your list mixes audit logging features, SIEM platforms, and compliance automation**, and several entries have no usable pricing.

## The data problems

**Druva Audit Logs is a feature, not a standalone platform.** Druva's Audit Trail lets administrators view user and admin activities, filter by activity type, and download CSV or HTML reports. Default retention is **30 days**, configurable; File & Folder activities retain for **3 months only** . Druva's starting price is listed at **$8.00/month** , but that is for the backup platform, not audit logging specifically.

**Splunk pricing is per GB/day, and the figure surfaced is for Enterprise, not ES.** CDW lists **Splunk Enterprise 1 GB/day at $8,694.99** . A separate listing shows **Splunk Cloud Enterprise Security 1 GB/day at $9,498.99** . **Do not present Splunk Enterprise as a SIEM price**—Enterprise Security is the SIEM product.

**Sumo Logic's Cloud SIEM ingest is 40 credits/GB**—the most expensive data type on the platform, higher than tracing (35) or standard logs (25). On the Credits model, credits list at **$0.25**; on Flex, they suggest **$1.50**. The two models **cannot be compared on credit counts alone** .

**AuditBoard and Panther are both quote-only with Vendr benchmarks.** AuditBoard median is **$45,947**; implementation adds **10–25%**; renewal escalation **3–7%** . Panther small-to-mid deployments (5–20 TB/month) typically pay **$50,000+**; onboarding services **$20,000–$100,000+**; renewal **3–8%** .

## What the search results actually contain

| Platform | Pricing | Verified detail |
|---|---|---|
| **Splunk Enterprise** | **$8,694.99 for 1 GB/day**  | Term license + Standard Success Plan |
| **Splunk Cloud ES** | **$9,498.99 for 1 GB/day**  | Enterprise Security, not Enterprise |
| **Datadog Cloud SIEM** | **$5.00 per 1M log events/month**  | 15-month analysis & retention |
| **Sumo Logic Cloud SIEM** | **40 credits/GB ingest**  | Most expensive data type; Flex credits ≠ Credits credits |
| **Elastic Security Serverless** | **$0.09–$0.11/GB ingest; $0.017–$0.019/GB retained**  | No per-endpoint fees as of March 2026 |
| **Papertrail** | **$7.00/month starting**  | Free plan available |
| **AuditBoard** | **$45,947 median**  | Implementation 10–25%; renewal 3–7% |
| **Panther** | **$50,000+ (5–20 TB/month)**  | Services $20K–$100K+; renewal 3–8% |

**Open-source projects (usable):**

| Project | What it actually does | Stars |
|---|---|---|
| **Graylog** | Open-source log management with audit trails; calculator shows **Open Source $368.8K/year for 1 TB/day, 90-day retention** vs **Enterprise $265.3K** (28% cost reduction)  | Not surfaced |

**What is missing:**
- **No pricing** for Druva Audit Logs as a standalone feature, LogRhythm, or Datadog beyond the per-million-event figure .
- **No star counts** for Graylog.
- **No pricing** for Elastic beyond serverless .
- **No information** on "Druva Audit Logs" as a distinct product—it is a feature of the backup platform .

## What I recommend

**Rename "Druva Audit Logs" to "Druva Audit Trail (feature)"** and note it is included with the backup platform, not sold separately .

**Split into three honest categories:**

**1. SIEM Platforms** (proprietary, priced per ingest): Splunk Enterprise/Cloud ES , Datadog Cloud SIEM , Sumo Logic , Elastic Security .

**2. Log Management** (proprietary): Papertrail ($7/month) .

**3. Compliance Automation** (proprietary, quote-only): AuditBoard ($45,947 median) , Panther ($50K+) .

**The open-source section has exactly one entry: Graylog.** It is a legitimate log management platform with audit capabilities, and the calculator shows Enterprise can be **cheaper than Open Source at scale** because of data reduction and cold storage . **Do not present Graylog Open Source as always cheaper**—the calculator explicitly shows the opposite for 1 TB/day workloads.

**Flag the pricing model differences explicitly:** per-GB/day (Splunk), per-million-events (Datadog), per-credit-by-data-type (Sumo Logic), per-GB-ingest (Elastic), and platform-wide (AuditBoard, Panther) produce wildly different costs at the same log volume. A reader choosing between them needs that context.

If you paste your current `README.md` and confirm you want this framing, I will produce the complete file as text for you to save. I will not fabricate star counts, present Druva Audit Logs as a standalone product, or label Splunk Enterprise pricing as Enterprise Security pricing.
