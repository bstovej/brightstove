---
layout: post
title: "Baseline Technical Measures for Data Privacy in the Cloud"
date: 2023-02-08 13:31:42
categories: [Data Privacy, Policy]
tags: [compliance, data protection]
---

<!-- wp:paragraph -->
<p>After several months of collaborative work with Prof Kwok-Yan Lam and Dr Chi-Hung Chi at NTU, and several data privacy and security practitioners in the industry, including Ivy Young of Amazon Web Services, Sam Goh of Data-X, Dr Zhan Wang of Envision Digital, Dr Prinya Hom-anek of TMBThanachart Bank, Dr Hing-Yan Lee and Daniele Catteddu of Cloud Security Alliance, and members of the Asia Cloud Computing Association (ACCA), I'm glad to share that the paper consolidating our findings on common privacy principles and proposed technical measures applicable for establishing a baseline for data privacy in the cloud is now published by the <a href="https://asiacloudcomputing.org/research/resources/" target="_blank" rel="noreferrer noopener">ACCA</a>. Below is the abstract and purpose of the paper. You may also watch a presentation of an earlier draft of this paper at the <a rel="noreferrer noopener" href="https://www.youtube.com/watch?v=99szU2xRGjE" target="_blank">HK/Macau CSA Summit (2022)</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:separator -->
<hr class="wp-block-separator has-alpha-channel-opacity" />
<!-- /wp:separator -->

<!-- wp:group {"layout":{"type":"constrained"}} -->
<div class="wp-block-group"><!-- wp:heading {"level":3} -->
<h3 class="wp-block-heading">Abstract</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>As the digital economy grows, individuals’ personal data is increasingly being collected, used, and disclosed, be it through online social media, e-commerce, or e-government transactions. As the volume of such personal data increases online, data breaches have become more prevalent, and consumers have increased their demands for stronger privacy protection. Data privacy legislations are not new—frameworks by the Organization for Economic Co-operation and Development (OECD), European Union General Data Protection Regulations (EU GDPR)<a href="#_ftn1" id="_ftnref1">[1]</a>, and Asia-Pacific Economic Cooperation (APEC) have existed as early as 1980. We have seen more policy developments being introduced recently across the global. In ASEAN, the Singapore Personal Data Protection Act (SG PDPA) was enacted more recently in 2012, and the latest being the Thailand Personal Data Protection Act (TH PDPA) that came into force on 1 June 2022.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Against the backdrop of these legal frameworks, businesses and governments are also leveraging advanced cloud services, such as AI/ML and Big Data Analytics to innovate and offer better customer services. As a result, more personal data is being migrated to the cloud, increasing the need for technical measures to enable privacy by design and by default and move beyond mere compliance with legal provisions. While new standards and frameworks have emerged to guide the management of privacy risk on the use of cloud, there are limitations in providing implementation guidance for technical controls to cloud using organizations. This paper thus seeks to fill the gap and provide technical measures that organizations may adopt to develop technical baselines that simplify their regulatory compliance across legal frameworks. We review the principles from the OECD, APEC, the EU GDPR, the SG PDPA, and the newly enforced TH PDPA, identifies a set of 31 technical measures that cloud using organizations may use to achieve common data protection objectives including fulfilling data subject rights, minimizing personal data exposure, preparing to respond to and recovering from data privacy breaches, ensuring security and quality of personal data, and providing transparency and assurance. Our elaboration of the technical measures for achieving these data protection objectives includes references to common cloud-enabled and cloud-native services from major CSPs to provide implementation guidance.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3 class="wp-block-heading">Purpose</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The motivation for this paper is to address the organizational needs for privacy compliance and fill the gaps in the existing standards. We adopt a principle-based methodology to identify a set of baseline technical measures suitable for achieving the data protection objectives underlying their privacy principles. The paper further presents guidance to cloud using organizations that cloud-native and cloud-enabled services may be used to implement the baseline technical controls with reference to capabilities available from major Cloud Service Providers (CSPs) including Amazon Web Services (AWS), Google Cloud Platform (GCP), and Microsoft Azure.</p>
<!-- /wp:paragraph -->

<!-- wp:separator -->
<hr class="wp-block-separator has-alpha-channel-opacity" />
<!-- /wp:separator -->

<!-- wp:paragraph -->
<p><a href="#_ftnref1" id="_ftn1">[1]</a> The GDPR repealed and replaced the Data Protection Directive, which was enacted in October 1995.</p>
<!-- /wp:paragraph --></div>
<!-- /wp:group -->