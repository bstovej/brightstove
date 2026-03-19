---
layout: post
title: Exploring the exposure management maze
date: 2026-03-19
categories:
  - Cybersecurity
  - Cyber Threat Intelligence (CTI)
  - Exposure Management
  - Vulnerability Management
created: 2025-03-17
modified: 2026-03-17T00:00:00
classification: public
summary: 'A deep dive into the Exposure Management landscape, demystifying the conflation of CTI, DRPS, and EASM through first principles of risk management and the intelligence cycle.'
status: completed
reviewed: true
last_reviewed: 2026-03-19 10:00
tags:
  - cybersecurity/risk_management/strategy
  - exposure_management
related:
  - "[[Understanding the Difference Threat Intelligence, DRPS, and EASM — A Practical Guide]]"
---
At the RSAC last year, I noticed that besides AI being the new buzzword in the cybersecurity market, many flavors of vulnerability management have emerged under the relatively new heading of "exposure management". Essentially, vendors have by then created a new category of service, separating vulnerability management from exposure management. The former as an internal view of exposures, and the latter as an external view of vulnerabilities. From External Attack Surface Management (EASM) to Digital Risk Protection Services (DRPS), Continuous Threat Exposure Management, Darkweb Monitoring, Brand Protection, and many more, some of these services have also been viewed as the subcategories of Cyber Threat Intelligence (CTI).

> "Complexity is the worst enemy of security. This is especially true for systems that are all interconnected." — *Bruce Schneier* [1]

While there may have overlaps in some of these services, for examples, DRPS, Darkweb Monitoring and Brand Protection, and CTEM and EASM, these exposure management services do serve more or less unique purpose. But are they vulnerability focused or threat focused? The answer seems to depend on how we phrase the question. If exposure management is about answering the question, "what are we *exposed to*", then it may invite an answer such as "we are exposed to <*list of threats or attacks*>". In other words, the question may be expanded to, "what *threats* are we exposed to?"

But if we ask, "what are our *exposures*?", then the likely answer will be "we have X numbers of critical *vulnerability*, Y number of high severity *vulnerability*, etc." 

Another way to understand the positioning of these services is to go back to the first principle, i.e., the risk equation that we are all familiar with. 

Security risk is commonly defined as a function of the relationship between threat, vulnerability, and impact, commonly expressed as:
$$Risk = f(Threat, Vulnerability, Impact)$$
When we view the services through this lens, their roles become clearer:

1. Cyber Threat Intelligence (CTI) identifies *Threat*. It focuses on the adversary—their motivations, capabilities, and Tactics, Techniques, and Procedures (TTPs). It answers: *Who is attacking us and how?*
2. External Attack Surface Management (EASM) identifies *Vulnerability* (or technical exposure). It focuses on the technical attack surface—inventorying internet-facing assets and identifying misconfigurations. It answers: *What do we own that is visible and potentially exploitable, in this case, externally?* The classical *Vulnerability Discovery* essentially covers the *internal* attack surface discovery. There are also new terms or services for such activities., e.g., *Breach Attack Simulation (BAS)*. That's a topic for another blog perhaps. 
3. Digital Risk Protection Services (DRPS) focuses on discovering *Impact* and the broader digital presence. It monitors the ecosystem, including the Darkweb, for brand abuse, leaked data, and fraud. It answers: *Has our data or brand been exploited in the wild?* A *Darkweb Monitoring* service if focused on brand alone would be a narrow part of DRPS, but if scoped beyond brand and data exposure, may help to discover threat actors' activities, including their new exploits, exploitation techniques, newly discovered vulnerabilities, and unreported breach incidents. 

In essence, in today's context, EASM and DRPS can be positioned as our "external sensors" that provide visibility of our organization's external state of exposure. The external nature of such exposure also means that such discovery often requires immediate, or high-speed actions from stakeholders at the operational layer of the organization such as IT Operations, Legal, and Brand Protection. If EASM identifies an open RDP port or DRPS identifies a typosquatting phishing site, the response must be immediate: patch the server or initiate a takedown. However, such data alone are usually insufficient for risk determination as vulnerabilities and impact are not sufficient to solve the risk equation. Understanding the risk aside, along with many other discoveries at the same time, it will also be a challenge to prioritize which issue to remediate first. This is where CTI comes in. CTI provides the threat perspective, closing the risk equation. As an analysis engine, CTI takes data from the external sensors and applying context to reduce noise and uncertainty. For example, while EASM might identify an exposed authentication portal, CTI provides the critical insight: *"This specific portal is currently being targeted by a known threat actor group active in S sector."* With the analytical layer of CTI providing the threat context, we we can devise a defense plan that addresses our actual risk exposure. Analytically, CTI further provides the strategic depth required to inform leadership of emerging risks and assists threat hunters in building more resilient detection logic. 

While catchy terms may provide freshness to old ideas, we need to peel back the layers to understand what they actually entail as a product or service. What are the capabilities that they provide? Are they adding to the complexity or creating new actionable insights? If we cannot distinguish between the adversary (Threat), our technical infrastructure weakness (Vulnerability), and our brand's presence (Impact), we are not managing risk—we are simply managing tools. Understand these nuances and integrate them into a cohesive whole are essential for building a truly responsive security posture.

For more insights on CTI, DRPS, and EASM, suggest reading the article: "Understanding the Difference Threat Intelligence, DRPS, and EASM — A Practical Guide". [2]

***
### References
[1] B. Schneier, *Secrets and Lies: Digital Security in a Networked World*. Wiley, 2000.

[2] Nicholas Tan, "Understanding the Difference: Threat Intelligence, DRPS, and EASM — A Practical Guide," *ThreatBook Blog*, 2026. Available at: "https://blog.threatbook.io/blog/threat-intelligence-drps-and-easm-a-practical-guide?hs_preview=EPXrygPr-314459615993"

