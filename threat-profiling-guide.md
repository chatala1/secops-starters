---
title: The Threat Actor Profile Guide for CTI Analysts
layout: home
parent: <b>Threat Intelligence</b>
---

# The Threat Actor Profile Guide for CTI Analysts

## Foreword

Threat actor profiles are made for a range of reasons. An example trigger for creating a new profile can include after an incident, e.g., an internal detection or supply chain breach has been observed. Alternatively, CTI research has identified that their organisation(s) or client(s) are likely to be targeted by the threat actor due to a number of factors.

The ‘Threat Actor Profile Guide for CTI Analysts’ was created after multiple Curated Intelligence members requested advice about the topic and their creation. Individuals in our community expressed difficulty and some shared their experiences around the difficulty of making one for their stakeholders.

This guide offers a templated introduction for CTI analysts getting started with profiling threat actors. Experienced CTI analysts and mature teams will likely have a more refined methodology and even different types of threat actor profiles tailored for a specific stakeholder type.

---

## Executive Summary

### Introduction

> “As of $Month 20XX, the Cyber Threat Intelligence team has researched the $ThreatActor”

- An Executive Summary should ideally be no longer than 10-15 lines (2-3 paragraphs)
- The main three questions to answer are:
  - **What?**
  - **So What?**
  - **What Now?**
- Explain the level of threat to the organisation, which includes:
  - Highlight whether the threat actor has targeted your organisation’s sector, country, or region as early as you can.
  - Make a short assessment of why your organisation could be targeted (or why they have been targeted) by the $ThreatActor.
  - Make a short evaluation of the ability of your organisation’s defence mechanisms to mitigate the threat.

---

### Executive Summary | Stakeholder Needs

#### The Executive Leadership Team (ELT)
- Talk about the potential losses that could be caused by a successful attack.
- Think about Intellectual Property Theft, Customer Data Theft, and Financial Theft.
- Focus on the impact to the organisation’s investments.

#### Operational (SOC, CERT, Security Engineering, Security Awareness, etc.)
- Talk about what tactics, techniques, and procedures (TTPs) that $ThreatActor uses.
- Highlight significant technical findings, like the fact that it exploits a certain CVE that is highly present in the organisation’s or client’s environment.

---

## About $ThreatActor

- Creating a Table of Threat Actor Aliases (sometimes referred to as cryptonyms) helps lay the foundation of the analysis in the profile.
- The Table helps readers quickly understand that multiple organisations are tracking what is essentially the same activity group using their own moniker.
- The analyst can discuss (and potentially use a diagram) if the attribution to a named threat actor the profile is for is not clearly defined elsewhere.
- For more guidance, Curated Intelligence has blogged previously on [Threat Actor Naming Schemes](https://www.curatedintel.org/2022/05/threat-group-naming-schemes-in-cyber.html).

Once the Threat Actor Alias housekeeping is done, the CTI analyst can begin to introduce the $ThreatActor.

The introduction should ultimately answer the following questions:
- What type of threat actor (group) is it? (e.g., Cybercrime, Espionage, Hacktivism, etc.)
- What areas does $ThreatActor specialise in?
- What type of campaign does $ThreatActor launch?
- Make a short assessment of how advanced the $ThreatActor is based on Reason X, Y, and Z.
- Discuss notable technical observations, such as software and TTPs.

---

## Targets of $ThreatActor

- Which sectors/verticals does $ThreatActor target?
  - Think: Proximity to our sector/region
  - Think: Recency of when their attacks were
- What does the $ThreatActor group do once they are inside a victim’s environment?
- How long have they been known to persist inside a victim’s environment?
- Are the targets of $ThreatActor related to each other?
  - Think: Cyber-enablement campaigns

---

## $ThreatActor Diamond Model Attributes

- The Diamond Model Attributes are the key pieces of information required to rapidly understand the $ThreatActor.
- After these are filled out by the CTI analyst, they can then be added to a Diamond Model Diagram.
- Once the Diagram is complete, the CTI analyst can introduce the threat actor and hit on the key points from their research and extraction of threat data.

**Diamond Model Components:**
- **Adversary:** Origin, Motivation, Activity
- **Victim:** Targeting, Locations, Systems
- **Capabilities:** IN, THROUGH, OUT
- **Infrastructure:** Attack Infrastructure, Support Infrastructure

---

## $ThreatActor Tactics, Techniques, and Procedures (TTPs)

- The first few lines of this section should include a summary of technical details at a high level that can be useful for all stakeholders.
  - This can be done by borrowing the Unified Kill Chain’s three stages: IN, THROUGH, and OUT ([Unified Kill Chain PDF](https://www.unifiedkillchain.com/assets/The-Unified-Kill-Chain.pdf))
- To discuss the $ThreatActor TTPs in detail, the MITRE ATT&CK framework is recommended ([MITRE ATT&CK](https://attack.mitre.org)).
- It is also recommended to create a table for TTPs: ATT&CK ID, Description, Observable, Source
- The point of this exercise is to demonstrate our technical understanding of the $ThreatActor.
- The TTPs can also be used for other activities by other stakeholders.
- Security Engineering will find these helpful in implementing detection for the activities.
- Red Teamers may use these for adversary emulation during engagements.
- The SOC will find these helpful for situational awareness and supporting their triaging of events.

---

## References

- Add all external references you intend to cite in your report.
- Use in-line citations to show the source of information (in paragraphs).
- Consider highlighting problematic sources and perform source evaluation.
  - This can be a footnote on a page of the threat actor card if there is contention around technical aspects or attribution assessments.
  - Only include if it is important for readers to know about.

---
