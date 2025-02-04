---
layout: ../../layouts/BlogPostLayout.astro
title: "Velocity with AI does not equal progress"
meta: "Velocity with AI does not equal progress | Blog | Talk to Me About Tech"
author: Sarah Conway
date: 02/03/2025
image: https://talktomeabouttech.com/images/velocity-with-ai-does-not-equal-progress.jpg
imagedesc: A cartoon image of a dog sitting with a cup of coffee in the middle of a raging dumpster fire, saying 'This is fine'
description: On cybersecurity, privacy, and legal risks of using AI as part of services or solutions.
---

So, now that 2025 has started, one of the first big announcements that has come out this year in the tech space is that Salesforce has officially decided:

“**We’re not adding any more software engineers next year because we have increased the productivity this year with Agentforce and with other AI technology that we’re using for engineering teams by more than 30% – to the point where our engineering velocity is incredible. I can’t believe what we’re achieving in engineering.**”

“**And then, we will have less support engineers next year because we have an agentic layer. We will have more salespeople next year because we really need to explain to people exactly the value that we can achieve with AI. So, we will probably add another 1,000 to 2,000 salespeople in the short term.**” 

*Marc Benioff ([source](https://www.salesforceben.com/salesforce-will-hire-no-more-software-engineers-in-2025-says-marc-benioff/))*

This is only one of the many examples of how AI is being implemented throughout companies, whether in internal operations or externally facing services. Is this a good idea? Bad idea? I’m sure you already have some opinions forming, but let’s break down some risks & considerations when deciding to implement AI within your operations or systems.

## The human element

Do humans make mistakes? Absolutely. However, so can AI systems. **It’s important to note that AI systems \- especially when implemented with known high error rates \- can lead to the mistreatment of your end-users (often with costly consequences for the company \- or incredibly detrimental consequences for the user).**

To begin with, you should be aware that assuming your consumers *want* AI as part of your offerings or solutions can be a mistake. End-users still have significant concerns when using AI technology, according to more than a few studies. As an example, an experimental study on "[Patients' Perceptions Toward Human-Artificial Intelligence Interaction in Health Care](https://pmc.ncbi.nlm.nih.gov/articles/PMC8663518/#sec30)" clearly showed that there were beliefs that "both AI applications and collective intelligence can lead to communication barriers", leading to a number of issues such as reduced communication on behalf of the consumer, a refusal to use AI applications, and increased concerns. 

Maybe you think they’re overreacting, or that they’re just afraid of technology like every other generation has been when approached with the new and strange. Yet, they *should* have these concerns. UnitedHealthcare (a year ago, now\!) purportedly denied care to elderly patients owed to them under Medicare Advantage Plans by "deploying an AI model known by the company to have a 90% error rate, overriding determinations made by the patients' physicians that the expenses were medically necessary." [*Source*](https://www.cbsnews.com/news/unitedhealth-lawsuit-ai-deny-claims-medicare-advantage-health-insurance-denials/)

This practice wasn't just isolated to UnitedHealthcare, and in fact shows up in multiple other lawsuits against [Humana](https://www.lawcommentary.com/articles/class-action-lawsuit-accuses-humana-of-using-faulty-algorithm-to-deny-claims), [Cigna](https://natlawreview.com/article/health-insurers-sued-over-use-artificial-intelligence-deny-medical-claims), and others following very similar patterns of consumers being denied insurance coverage over arbitrary rules or pre-set definitions fed to AI algorithms.

The takeaway? Test your systems and really walk through the user experience. Can you trick the AI into doing something it shouldn’t be able to? How accurate is the output? 

*Are you really doing your users a favor by implementing this into your service offering or internal operations?*

*What are the consequences if it goes wrong, to our company and to our users?*

## Cybersecurity attacks

AI is no less susceptible to security breaches and cybersecurity attacks than other technologies. Attacks against these systems are "enabled by inherent limitations in the underlying AI algorithms that currently cannot be fixed." This can result in attacks against the AI system itself, leading to situations such as hackers exploiting AI vulnerabilities to get money ([$50,000 in one case](https://www.geeky-gadgets.com/hacker-manipulates-ai-for-cryptocurrency/), for example). 

In other cases, it can lead to humans manipulating AI behaviors to attack other humans \- for example, placing a "few pieces of tape on the stop sign itself" can "transform a stop sign into a green light in the eyes of a self-driving car." [*Source*](https://www.belfercenter.org/publication/AttackingAI)

And of course, because code is being released at such a rapid rate, it’s incredibly easy for zero-day vulnerabilities to be exploited in LLM models. One of the latest examples (as of this article's date)? "AI frameworks, including Meta’s Llama, are prone to automatic Python deserialization by pickle that could lead to remote code execution." [*Source*](https://www.csoonline.com/article/3810362/a-pickle-in-metas-llm-code-could-allow-rce-attacks.html)

Even after that vulnerability, breaking news occurred almost immediately over the latest LLM to gather international recognition almost overnight \- DeepSeek. This LLM almost immediately after its release was discovered to have a publicly accessible ClickHouse internal database server that exposed "highly sensitive information, including secret keys, plain-text chat messages, backend details, and logs." [*Source*](https://cybersecuritynews.com/deepseek-database-leaked/)

Before companies roll out the use of AI in high-risk situations with critical implications, *we must as a society decide to mandate compliance to mitigate security concerns.* **This pattern of releasing without taking a moment to consider what could happen in the event of a cybersecurity attack** \- to either the company itself, or the end users\! \- **must end.**

And until it does, we should take a moment, collectively, to work on improving AI models and making them inherently more secure.

## On ethics & privacy considerations

From many sources, there are significant concerns that have risen around the belief that personally identifying information is being collected or shared without permission for purposes other than treatment (or otherwise, that anonymized data can be re-identified). 

Is there any basis to these concerns? Well, yes.

[There are a host of lawsuits open at this very moment](https://sustainabletechpartner.com/topics/ai/generative-ai-lawsuit-timeline/), including many that claim AI providers are "unlawfully collecting and using peoples' personal data to train their artificial intelligence (AI) models". 

And, yes, data that was anonymized can still be used to identify users. The [Georgetown Law Technology Review](https://www.isaca.org/resources/news-and-trends/industry-news/2024/reidentifying-the-anonymized-ethical-hacking-challenges-in-ai-data-training) found that 99.98% of Americans could be reidentified from a dataset using just 15 basic attributes. Reading a little further into the study itself, we find:

\> …scrubbed data can now be traced back to the individual user to whom it relates. Scrubbed data is commonly re-identified by combining two or more sets of data to find the same user in both. This combined information often reveals directly identifying information about an individual.  
[*Source*](https://georgetownlawtechreview.org/re-identification-of-anonymized-data/GLTR-04-2017/)

Many companies have announced the collection of user data for training AI systems incorrectly or without properly addressing GDPR or other privacy constraints & regulations, and as a result [experienced a huge backlash from the user base](https://arstechnica.com/tech-policy/2024/05/slack-defends-default-opt-in-for-ai-training-on-chats-amid-user-outrage/) (with good reason). 

*OK, so what actions can be taken to prevent negative repercussions?*

1. If you are collecting users’ data or are using datasets to train AI systems, stay compliant with privacy regulations like the GDPR or CCPA.  
2. Don’t assume that users are going to be pleased that you’re collecting their data, even if you are taking excessive steps to protect their privacy. **Implement an easy-to-find, and easy to use opt-out button.** Don’t make your users jump through hoops to prevent the unauthorized use of their data.  
3. While you’re doing that, make it explicitly clear what data is being collected for what purposes, and make sure your users are completely aware.

## Choosing a LLM

A note: the LLM you end up choosing can have an enormous impact on all of the above concerns.

For example, there is always “...the potential to perpetuate harm. Typically trained on an enormous scale of uncurated Internet-based data, LLMs inherit stereotypes, misrepresentations, derogatory and exclusionary language, and other denigrating behaviors that disproportionately affect already-vulnerable and marginalized communities (Bender et al. 2021; Dodge et al. 2021; Sheng et al. 2021b).” [*Source*](http://direct.mit.edu/coli/article/50/3/1097/121961/Bias-and-Fairness-in-Large-Language-Models-A)

Whenever possible, train your models on your own data and systems / processes; you’ll avoid a lot of issues and bias that accompany the inaccuracy of these models. And, really take some time to research the LLM you choose for your solution. As a result, you should experience less risk.

## Takeaways

Ultimately, some use of AI *may in fact be useful for your business*. This article isn’t meant to dissuade you from that conclusion. 

What this article *is* meant to do is help you make a decision that won’t lead to incredibly harmful impacts for you and your company, or your end-users.

**Decide what’s best for your goals**

*Don’t implement AI into your internal tech stack or service offerings just because it’s cool.* You may find it causes far more problems than you end up solving.

If you decide that it makes sense in your use case to leverage AI technology, it’s important to recognize the value of…

* using humans to fact-check your AI systems,   
* implementing stringent security policies to protect both the company and the end users, and   
* not overstepping and violating privacy regulations to better your own product. 

**Need consulting or assistance in engineering the best experience for your end-users while protecting your company from risks?**

Feel free to reach out via [email](mailto:info@talktomeabouttech.com) or [schedule a free 1:1 call](https://lets-talk-about-tech.neetocal.com/initial-consultation-call); we’d be happy to help you mitigate risk and choose a great solution for your use case.