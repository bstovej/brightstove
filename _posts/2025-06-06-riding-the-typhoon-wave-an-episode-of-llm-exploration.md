---
layout: post
title: "Riding the Typhoon wave: An episode of LLM exploration"
date: 2025-06-06 13:24:33
categories: [AI Risk, AI Security, AI Governance]
tags: [AI risk, cybersecurity]
---

Was exploring a few open source LLMs installed in my laptop and observed some strange behaviors. Maybe someone here can help to explain why. More importantly, the episode reinforced the following to keep in mind when using LLM chatbots:

1. Craft the prompt carefully upfront. Be as specific as possible. Avoid using general terms, which will get general responses.
2. After getting the response, turn off the web search if what you need the LLM to do next is to work on those responses instead of finding new input.
3. Start a new chat window when moving to a new context to avoid confusing the LLM.
4. For better results, use specialized/fine-tuned LLM for tasks that are in a specialized domain.
5. If you have RAG setup, use it to analyze instead of just using the web search feature, which should produce better results.

The original post was published at [Substack](https://substack.com/profile/324848066-meng-chow-kang/note/c-123368408). Here's the full article:

---

The Typhoon threat groups, which consists of several names such as Salt, Volt, and Flax Typhoon, have made wave recently in the critical infrastructure industry although there have been reports about their activities as early as in 2021 @hongsiangSingtelDetectedEradicated2024; @htelAPT41WickedPanda2025; @kimuraVoltTyphoonBRONZE2025; @yellandVoltTyphoonSalt2025;. Using [SecAI’s AI-powered threat intelligence enabled chatbot](https://i.secai.ai/), with a simple prompt, we can quickly get a comprehensive report of what the threat groups are and the commonly known techniques, tactics, and procedures (TTP) attributed to them. For example, with the prompt, "*what can you tell me about the Typhoon threat group?*" SecAI provides a curated report of everything it knows from the Internet and its cyber threat intelligence (CTI) database. A snippet of the report reads as follows:

> *The Typhoon threat groups consist of multiple Advanced Persistent Threat (APT) entities generally attributed to China and linked to state-sponsored cyber espionage efforts. These groups have shown high levels of sophistication in targeting critical infrastructure, government agencies, and corporate sectors worldwide. Below is a comprehensive breakdown of the Typhoon threat groups, including key actors such as Salt Typhoon, Volt Typhoon, Flax Typhoon, Velvet Ant, and others. ... 

The SecAI chabot further elaborates individual threat group sharing certain attributes as the other Typhoon groups, followed by an assessment of the groups' impact, and recommendation of defensive measures that can be adopted against them. Relevant web links are also listed in the response for further reading. The full SecAI report can be found [here](https://i.secai.ai/share?threadId=718bd3d38c3144d78b15bda317692b81) or retrieved simply by going to the SecAI.ai site and type in the above prompt.

This essentially satisfies any curiosity about the Typhoon threat actor groups and what we can do about it to minimize our risk of falling victim to it.

While tinkering with my local open source LLMs setup using Ollama and OpenWebUI, I thought, why not check out the open source LLMs that are not fine-tuned with CTI knowledge to see how they performed against SecAI’s chatbot. Using OpenWebUI, comparing the output of different LLMs is straightforward. I just need to add the LLM models in the chat window before entering the prompt. Using Llama 3.2:latest, Mistral-Large-2411, and Deepseek-r:1.5b, I input the same prompt, "*what can you tell me about the Typhoon threat group?*" What follows are some interesting observations of the responses from the three LLMs.

After searching 15 and 20 sites, respectively, llama3.2 and mistral-large proceeded to report what they know about the threat actor groups. Unlike SecAI's, the two LLMs output are more abstract, providing a quick summary of the related groups, as shown in the screenshot below. 

Deepseek-r1 however provides an entirely different response, stating that the *Typhoon Threat Group is an organization dedicated to evaluating the threat posed by tropical cyclones to global weather systems...* ". See partial screenshot of the responses from the three LLMs below.

Typhoon, in this context, is the name of a cybersecurity threat group and I've mentioned "threat group" in the prompt. I have also enabled the web search feature and Deepseek-r1 did generate search queries and reported that it has searched 46 sites. It however decides not to use the results of the web search to enhance the context, and presents its output along the line of the meteorological typhoon. Did Deepseek not fully comprehend the context of the prompt, or is it some kind of "self-protection guardrail"? I wonder.

Maybe this shouldn't be a surprise. Since its launch in early 2025, there have been several reports that Deepseek exercises self-censorship @boothChineseAIChatbot2025; @roeloffsDoesDeepSeekCensor2025; @yangDeepSeekYouCan2025;.


![Sample response from three LLMs]({{"/assets/images/screenshot-2025-05-20.png"| relative_url }})
*Figure 1: Sample response from three LLMs*

In any case, I left it as is, locked the screen, and went for lunch. 

After lunch, I was thinking about an AI threat modeling exercise for another project. Since the three LLM models were running at this point, perhaps I can just let them tell me something about AI related threats before I do my own digging. So I entered the prompt, "*what are the threats relating to AI systems, in particular, in LLM applications developments, deployment, and use?*"

After completing its search at 30 sites, llama3.2 presents a list of 10 threats and six mitigating measures. The threat list are: (1) bias and fairness, (2) security and privacy, (3) misinformation and disinformation, (4) explainability and transparency, (5) cybersecurity risks, (6) intellectual property concerns, (7) ethical considerations, (8) job displacement and economic impact, (9) dependence on technology, and (10) culture homogenization--*risk of cultural assimilation due to the widespread adoption of LLMs, potentially leading to loss of diverse linguistic and cultural expressions.* I didn't expect this list to be the response, since by means of "threats relating to AI systems", I was thinking about cybersecurity threats, but missed the cybersecurity word in my prompt and so it results in the LLM reporting a much broader spectrum of related threats. Differentiating "security and privacy" and "cybersecurity risk" is also unexpected. The former includes "data breaches or unauthorized access, AI-powered phishing attacks, and risk of model manipulation", whereas the latter cites "*vulnerabilities in AI systems can be exploited by malicious attacks, leading to significant security breaches"* . 

Mistral-large-2411 was however able to interpret the cybersecurity context of the question accurately. After searching 28 sites, presents 17 cybersecurity and privacy threats. I think it is a useful list so I'm including it as an appendix to this blog for reference. Mistral-large-2411 did not suggest any mitigating measures for addressing those threats.

Deepseek-r1 searches 10 sites and reports that it "*thought for 7 seconds*" then presents its findings of 13 "threats" with a few that overlaps with the llama3.2 list. Deepseek-r1 however presents its threat list in a slightly different format. For example, see table below. 

| **Llama3.2** | **Deepseek-r1** |
| :--- | :--- |
| **Security and Privacy**:<br><br>- Data breaches or unauthorized access to sensitive information stored in LLMs.<br>- Potential for AI-powered phishing attacks or malware spreading through language-generated content.<br>- Risk of model manipulation or tampering by malicious actors. | **Cybersecurity Threats**<br><br>- **AI-based Threat Detection and Anomaly Detection**: LLMs can analyze vast amounts of data, including social media sentiment, network traffic, and system logs, to detect anomalies or malicious activities.<br>- **Fraud Detection**: AI-driven systems can predict fraudulent transactions by analyzing patterns in transaction histories, user behavior, and account details.<br>- **Phishing and Manipulation**: LLMs can be trained on large datasets of spammed emails, surveillance feeds, and other forms of fake communication to perform phishing attacks or manipulate information.<br>- **Data Breaches**: As AI models become more powerful, they may be used to intercept sensitive personal data, breach login credentials, or even disrupt communication. |
| **Job Displacement and Economic Impact**:<br>- Automation of jobs that were previously done by humans, potentially leading to unemployment.<br>- Disruption of industries due to LLM's ability to generate high-quality content quickly and efficiently. | **Job Displacement and Economic Threats**<br><br>- **AI in Manufacturing and Trade**: LLMs can optimize supply chains, reduce costs, and improve efficiency in industries like automotive, manufacturing, and agriculture.<br>- **Automation in Services**: While automation reduces labor costs, it may also lead to job losses or displacement of workers who were previously relied upon for essential functions.<br>- **Job Scams**: Misuse of AI-driven systems in recruitment or employment could result in unethical hiring practices. |

Deepseek-r1 mentions specific industry or application area, and calls out the benefits of AI in each area, e.g., threat and anomaly detection, optimize supply chains, reduce costs, etc., before highlighting the related threats. Llama3.2 simply summarizes the threats in each category.

What's interesting is that Deepseek-r1 added "*environmental and climate change threats*" to its list. Has it been influenced by the earlier Typhoon prompt since I did not switch to a new chat window to ask the threats to AI questions? I didn't think about this question until what happened next when I prompted the three models to "*Categorise each threat in terms of its applicability to LLM applications development, deployment, or use; and output in the form of a table.*"

This is a simple follow-up question that only needs the LLMs to restructure its earlier responses. Somehow, something puzzling happens. Llama3.2 adds an "Environmental and Climate Change Threats" and a "Potential Expansion" threat to its list of 10, totaling 12. "Potential Expansion" threat is one of the items in Deepseek-r1's earlier threat list. 

In respond to this prompt, Mistral-large-2411 also changes its threat list entirely to read like the Deepseek-r1's earlier list, including the "Environmental and Climate Change Threats", and an additional "Ethical Guidelines and Standards" threat item. 

While Llama3.2 and Mistral-large-2411 adopt a higher-level view of the threats involved, and are now closer in their output to the Deepseek-r1 threat list, Deepseek-r1 changes its list entirely into a new list of eight threat items: (1) Insufficient datasets, (2) Data privacy concerns, (3) Eithical issues with LLMs, (4) Inadequate datasets for deployment, (5) Unintended misuses of AI, (6) Overuse of AI technology, (7) Accessibility issues, and (8) AI as a tool for disinformation. 

Such output changes are quite odd. Not sure if there is a term for such a change of behavior within an ongoing interactive context. As web search was enabled and performed by the LLM after each prompt, it could be that the prompt resulted in a near similar search results for the Llama3.2 and Mistral this time, but completely different result for Deepseek-r1 that led them to change their output. But this hypothesis doesn't seem to hold since the number of sites searched for the three LLMs are 30, 41, and 90, respectively. 

Maybe some readers have an explanation for such odd behaviors, which run across not just one particular LLM, but all three, notwithstanding the special output specific to the Typhoon question that is unique to Deepseek-r1. Or maybe its OpenWebUI handling of the prompts, memory, etc., that needs some special care to be taken when using multiple LLMs at the same time. Would be glad to hear from anyone who have an insight on this.

In any case, reflecting from this episode, there are a few things that I think worth keeping in mind when using the LLM chatbots:
1. Craft the prompt carefully upfront. Be as specific as possible. Avoid using general terms, which will get general responses.
2. After getting the response, turn off the web search if what you want the LLM to do next is to work on those responses instead of finding new input.
3. Start a new chat window when moving to a new context to avoid confusing the LLM.
4. For better results, use specialized/fine-tuned LLM for tasks that are in a specialized domain. An example is the SecAI's Chatbot and Investigator that I've mentioned at the beginning of this post. The SecAI tools are specifically fine-tuned and trained for CTI and cybersecurity investigation related tasks.
5. I should have used my collection of AI cybersecurity articles and reports as the knowledge base in OpenWebUI for the LLM to analyze instead of just using the web search feature, which should produce better results. But the test was impromptu and I didn't think too much about using RAG that is readily available. That's another lesson learnt :-P

---
**Appendix - Threats relating to AI systems collated by Mistral-large-2411**
Prompt:
- *What are the threats relating to AI systems, in particular, in LLM applications developments, deployment, and use?*

Response from mistral-large-2411:

> There are several key threats relating to AI systems, particularly in the context of LLM (Large Language Model) applications. These threats span various layers of the AI ecosystem, including development, deployment, and usage:
> 
> 1. **Prompt Injection (LLM01:2025)**: This is one of the most common attacks targeting the input layer of LLM applications. It involves injecting malicious prompts to manipulate the model's output.
> 2. **Excessive Autonomy**: As LLM applications gain more autonomy, there is an increased risk of excessive agency, where the model may perform actions beyond its intended scope, leading to unintended consequences.
> 3. **RAG Vulnerabilities**: With many companies opting not to fine-tune their models and relying on Retrieval Augmented Generation (RAG) and Agentic pipelines, vulnerabilities related to vector and embedding weaknesses have become more prominent.
> 4. **System Prompt Risks**: Leakage of system prompts can expose sensitive information, making it crucial to manage what is included in these prompts.
> 5. **Unbounded Consumption**: The widespread enterprise adoption of LLMs has led to resource management challenges, termed "unbounded consumption," where the surge in resource usage can overwhelm infrastructure.
> 6. **Compromised Container Images**: Malicious code injected into AI agent containers can infect production systems, compromising the AI deployment environment.
> 7. **Orchestration Attacks**: Exploiting vulnerabilities in systems like Kubernetes can give unauthorized access and control over AI deployment systems, disrupting AI agent functionality.
> 8. **Infrastructure-as-Code (IaC) Manipulation**: Tampering with scripts used to provision AI resources can lead to the creation of insecure deployment infrastructure for AI agents.
> 9. **Denial of Service (DoS) Attacks**: Overwhelming infrastructure resources supporting AI agents can cause the AI systems to become unavailable to legitimate users.
> 10. **Resource Hijacking**: Attackers can use compromised AI infrastructure for cryptomining or other illicit purposes, leading to performance degradation of AI agents.
> 11. **Lateral Movement**: Attackers gaining access to one part of the AI infrastructure and then using that access to compromise other sensitive AI areas can lead to further compromise of additional systems and data in the AI ecosystem.
> 12. **Compromised Framework Components**: Malicious code in libraries or modules used by AI frameworks can compromise the functionality of the framework, leading to unexpected results.
> 13. **Backdoor Attacks**: Hidden vulnerabilities or functionalities in the AI framework can be exploited by attackers to gain unauthorized access and control over AI agents.
> 14. **Input Validation Attacks**: Exploiting weaknesses in how the AI framework handles user inputs can allow for code injection and potential system compromise of AI agent systems.
> 15. **Supply Chain Attacks**: Targeting the AI framework’s dependencies can compromise software before delivery and distribution, resulting in compromised AI agent software.
> 16. **Denial of Service on Framework APIs**: Disrupting the AI framework’s ability to function by overloading services can prevent normal operation for the AI agents.
> 17. **Framework Evasion**: AI agents specifically designed to bypass security controls within the framework can use advanced techniques to perform unauthorized actions .
> 
> These threats highlight the need for robust security measures and continuous monitoring to mitigate risks associated with LLM applications and AI systems.

#### References 
[1] N. Hong Siang, “Singtel detected and ‘eradicated’ malware said to be from Chinese hacking group,” _CNA_, Nov. 05, 2024. Available: [https://www.channelnewsasia.com/singapore/singtel-malware-chinese-hacking-group-volt-typhoon-4724931](https://www.channelnewsasia.com/singapore/singtel-malware-chinese-hacking-group-volt-typhoon-4724931). [Accessed: Jun. 04, 2025]

[2] K. P. Htel and N. Rostovcev, “APT41, Wicked Panda, Brass Typhoon, BARIUM, Group G0096 | MITRE ATT&CK®,” _MITRE ATT&CK_, Apr. 22, 2025. Available: [https://attack.mitre.org/groups/G0096/](https://attack.mitre.org/groups/G0096/). [Accessed: Jun. 04, 2025]

[3] A. Kimura, M. Srinivasan, P. Natarajah, and V. Shumaher, “Volt Typhoon, BRONZE SILHOUETTE, Vanguard Panda, DEV-0391, UNC3236, Voltzite, Insidious Taurus, Group G1017 | MITRE ATT&CK®,” _MITRE ATT&CK_, Apr. 30, 2025. Available: [https://attack.mitre.org/groups/G1017/](https://attack.mitre.org/groups/G1017/). [Accessed: Jun. 04, 2025]

[4] M. Yelland, “Volt Typhoon, Salt Typhoon & APT41: This is No Longer a Drill,” MixMode, Inc, Threat Report, Apr. 2025. Available: [https://mixmode.ai/blog/volt-typhoon-salt-typhoon-apt41-this-is-no-longer-a-drill/](https://mixmode.ai/blog/volt-typhoon-salt-typhoon-apt41-this-is-no-longer-a-drill/). [Accessed: Jun. 04, 2025]

[5] R. Booth and D. Milmo, “Chinese AI chatbot DeepSeek censors itself in realtime, users report,” _The Guardian_, Jan. 28, 2025. Available: [https://www.theguardian.com/technology/2025/jan/28/chinese-ai-chatbot-deepseek-censors-itself-in-realtime-users-report](https://www.theguardian.com/technology/2025/jan/28/chinese-ai-chatbot-deepseek-censors-itself-in-realtime-users-report). [Accessed: Jun. 04, 2025]

[6] M. W. Roeloffs, “Does DeepSeek Censor Its AI Answers? On These Sensitive Topics, Yes.,” _Forbes_, Jan. 27, 2025. Available: [https://www.forbes.com/sites/maryroeloffs/2025/01/27/does-deepseek-censor-its-answers-we-asked-5-questions-on-sensitive-china-topics/](https://www.forbes.com/sites/maryroeloffs/2025/01/27/does-deepseek-censor-its-answers-we-asked-5-questions-on-sensitive-china-topics/). [Accessed: Jun. 04, 2025]

[7] A. Yang, “On DeepSeek, you can watch AI navigate censorship in real time,” _NBC News_, Jan. 30, 2025. Available: [https://www.nbcnews.com/tech/innovation/deepseek-censorship-china-rcna189594](https://www.nbcnews.com/tech/innovation/deepseek-censorship-china-rcna189594). [Accessed: Jun. 04, 2025]
