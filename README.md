#### Library Main Navigation: &nbsp; &nbsp;  <b>  [Ecosystem Library Home](https://github.com/NIH-NICHD-Ecosystem) </b> &nbsp; | &nbsp;[User Stories](https://github.com/NIH-NICHD-Ecosystem/UserStories/blob/main/README.md) &nbsp; | &nbsp; [Efforts](https://github.com/NIH-NICHD-Ecosystem/Efforts/blob/main/README.md) &nbsp; | &nbsp; [Library Help](https://github.com/NIH-NICHD-Ecosystem/LibraryHelp/blob/main/README.md)

</br>

# E6: Protecting scientific data when using generative AI

### This effort is a summary of how biomedical data protection obligations may conflict with the research community’s use of public GenAI tools based on company-wide or tool-specific privacy policies and terms of service/use, as well as the nature of the underlying large language models. It examines three potential sources of data protection rules common to biomedical research involving human data and compares them to common principles in GenAI policies, terms, and related literature regarding how data inputs and outputs are handled to illustrate risks that the research community should consider.  Awareness of these challenges can inform how researchers, scientific data repositories, and organizations engage with both public and private instances of GenAI tools.

</br>

# Table of Contents

- [Effort Overview](#effort-overview): high-level details and contact information
  - Effort Overview
  - Primary Contact
  - Details
- [Biomedical Data Protection Rules](#Biomedical-Data-Protection-Rules)
- [Analysis](#Analysis)
- [User Stories](#user-stories)

<br/><br/>

# Effort Overview 
The rapid popularization of ChatGPT and other generative AI (GenAI) technologies based on large language models (LLMs) offer enticing opportunities for biomedical research. The research community must protect sensitive data they may wish to use in these tools. The Eunice Kennedy Shriver National Institute for Child Health and Human Development (NICHD) Office of Data Science and Sharing (ODSS) has analyzed the privacy policies and terms of service/use of several public LLM-based GenAI tools and considered literature regarding re-identification as well as memorization and leakage of model training data to identify potential conflicts with  data protection obligations common in biomedical research. 

#### Primary contact:  _[NICHDecosystem@nih.gov](mailto:NICHDecosystem@nih.gov)_<br/>

#### Details: 
* <b> Created and maintained by:</b> NICHD ODSS  </br>
* <b> NIH contacts:</b>
    * Valerie Cotton, Deputy Director, NICHD ODSS

<br/><br/>

# Biomedical Data Protection Rules
Depending on the data source and which stage of the data lifecycle they are in, a researcher may need to comply with the Health Insurance Portability and Accountability Act (HIPAA),  the HHS Policy for the Protection of Human Subjects (also known as the Common Rule),  associated Institutional Review Board (IRB) determinations and promises made via participant consent, as well as rules that apply to data shared through controlled access scientific data repositories (e.g., NIH’s database of Genotypes and Phenotypes [dbGaP]), even if de-identified  (Figure 1). These rules prohibit unauthorized disclosures and uses among other requirements, which sometimes conflict with how GenAI tools and companies handle data inputs and outputs (Figure 2). 

HIPAA and the Common Rule generally govern handling of identifiable information about patients or research participants, but some IRB determinations and consent provisions also impact how de-identified data must be handled (e.g., used only to study a specific condition, strategies for mitigating re-identification). Scientific data shared through controlled access data repositories are typically de-identified but the repositories must enforce and adhere to data protections, any upstream rules (e.g., those inherited from IRB determinations or consents), as well as additional requirements (e.g., specific security safeguards). A researcher may need to navigate additional rules in their research (e.g., other laws, institutional policies).

</br>

![Figure 1](https://github.com/NIH-NICHD-Ecosystem/E6-Protecting-scientific-data-when-using-generative-AI/blob/main/assets/datalifecycle.png)

_**Figure 1. Rules & Activities across the Scientific Data Lifecycle.** A researcher may be subject to HIPAA (e.g., for data extracted from hospital electronic health records), the Common Rule, related IRB determinations and consent form provisions, and a data use agreement and other requirements for using data from controlled access scientific data repositories, even if de-identified. Data repositories and their curators must also secure the data they process and share, even if de-identified._

<br/><br/>


# Analysis
Figure 2 summarizes an analysis of potential conflicts with common biomedical data protection rules when the research community inputs data into public GenAI tools. 

<br/><br/>
![Figure 2](https://github.com/NIH-NICHD-Ecosystem/E6-Protecting-scientific-data-when-using-generative-AI/blob/main/assets/genaiRules.png)
<br/>
_**Figure 2. Conflicts with Data Protection Rules when Using Public Generative Artificial Intelligence Tools in Biomedical Research.** The left side describes common principles for how public GenAI tools and their companies handle data, the right side lists common biomedical data protection rules, and arrows connecting them represent conflicts. Bold arrows on the left side connect related principles that impact the interpretation of conflicts. Principles and conflicts relevant to data used to train models are colored purple or green. Rules on the right are tagged as deriving from “HIPAA”, Common Rule (which are tagged as “IRB/consent” to emphasize the importance and potential variability of IRB determinations and consent provisions in implementing the Common Rule), and/or “CAD” for data from controlled access scientific data repositories._

</br>

GenAI companies **access, use, retain,** and **disclose** data inputted into, and generated by, their tools for a wide variety of reasons (Table 1a) even when industry security standards are in place. They are also permitted or required to disclose (or “share”) the data with a number of internal and external parties (Table 1b). 

Many privacy policies and terms of service for public GenAI companies are common for other public and commercial digital tools, including those that are not AI-based, and are often focused on how the user’s personal information is handled. What makes GenAI unique is that the scope of data covered by these policies and terms includes **inputs** from the user and associated model **outputs** which could include sensitive information about someone who is not the user, such as research participants represented in the data.

**Table 1. Common allowable uses and disclosures in public GenAI policies and terms.**
| a. Common allowable uses of public GenAI tool data inputs and outputs | b. Common allowable disclosures: Parties and entities who may access the data inputs and outputs  |
| :------------ | :------------- |
| <ul><li> host, copy, reproduce, distribute, communicate, and use the data </li></ul><ul><li>disclose or “share” data with internal and external parties/entities (examples listed column b) </li></ul><ul><li>provide, maintain, facilitate, repair, and improve the tool and related services  </li></ul><ul><li> monitor product performance  </li></ul><ul><li> develop new products, services, and machine-learning technologies  </li></ul><ul><li>develop new features  </li></ul><ul><li>compliance purposes  </li></ul><ul><li>detect violations of and enforce compliance with terms and policies (e.g., preventing harm)  </li></ul><ul><li>detect, prevent, investigate and respond to fraud, abuse, unlawful or criminal activity, malicious activity, and security incidents  </li></ul><ul><li>detect, prevent, investigate and respond to technical issues   </li></ul><ul><li>safety monitoring  </li></ul><ul><li>prevent harm to the company, its products, its users, or the public  </li></ul><ul><li>handle legal matters   </li></ul><ul><li>comply with law  </li></ul><ul><li>provide user account support  </li></ul><ul><li>exchange information with connected tools and applications  </li></ul><ul><li>personalize content  </li></ul><ul><li>customize search  </li></ul><ul><li>human or automated review  </li></ul><ul><li>advertising   </li></ul><ul><li>retain the data for as long as needed _(even beyond defined durations if needed to support certain activities, such as those listed above)_  </li></ul><ul><li> **model training** _(can sometimes be disabled under certain conditions)_ </li></ul> |  <ul><li> host, copy, reproduce, distribute, communicate, and use the data </li></ul><ul><li>disclose or “share” data with internal and external parties/entities (examples listed column b) </li></ul><ul><li>provide, maintain, facilitate, repair, and improve the tool and related services  </li></ul><ul><li>monitor product performance  </li></ul><ul><li> develop new products, services, and machine-learning technologies  </li></ul><ul><li>develop new features  </li></ul>
<ul><li>compliance purposes  </li></ul><ul><li>detect violations of and enforce compliance with terms and policies (e.g., preventing harm)  </li></ul><ul><li>detect, prevent, investigate and respond to fraud, abuse, unlawful or criminal activity, malicious activity, and security incidents  </li></ul><ul><li>detect, prevent, investigate and respond to technical issues   </li></ul><ul><li>safety monitoring  </li></ul>
<ul><li>prevent harm to the company, its products, its users, or the public  </li></ul><ul><li>handle legal matters   </li></ul><ul><li>comply with law  </li></ul><ul><li>provide user account support  </li></ul><ul><li>exchange information with connected tools and applications  </li></ul><ul><li>personalize content  </li></ul><ul><li>customize search  </li></ul><ul><li>human or automated review  </li></ul><ul><li>advertising   </li></ul><ul><li>retain the data for as long as needed _(even beyond defined durations if needed to support certain activities, such as those listed above)_  </li></ul><ul><li> **model training** _(can sometimes be disabled under certain conditions)_ </li></ul> | 
 <ul><li> Company employees, contractors, vendors, and agents (sometimes only “authorized personnel”) </li></ul><ul><li>Company affiliates, subsidiaries, or successors </li></ul><ul><li>Service providers (e.g., those that provide website or data hosting and other IT services, customer service, audits, safety monitoring services, and search providers) </li></ul><ul><li>Federal government authorities or regulatory bodies </li></ul><ul><li>International government entities </li></ul><ul><li>Other trusted businesses or persons </li></ul><ul><li>“Other third parties”   </li></ul>| 

Many of these uses and disclosures are intended to benefit the user and/or the public (e.g., safety, fraud detection, harm prevention, legal reasons). However, they may conflict with a researcher's obligation to protect the data, which usually requires restricting access to only approved users and controlling how the data is used (Figure 2).  While the company and tool policies and terms are enforceable by Federal Trade Commission laws around deception and fairness,   determining when these uses and disclosures occur may be at the company’s discretion thereby limiting a researcher's ability to predict whether, how, and for how long the data may be accessed, used, retained, and disclosed by GenAI companies. Additionally, these uses and disclosures are not considered a “breach” by the company. Companies are subject to (usually state-specific) breach notifications laws which typically only require notification to users in specific situations (e.g., unauthorized access of personal information that poses unreasonable risk of harm).   

Most of the GenAI terms and policies apply even when model training with inputs/outputs is disabled, but when **model training** is enabled, the potential for other users to access sensitive training data using specific prompts or other methods, whether inadvertently or intentionally, raises additional risks for unauthorized disclosure and unallowable use of the data. Several groups have demonstrated ways sensitive information used as training data can be memorized and subsequently “leaked” as outputs.  Even when additional steps are taken to mitigate such leakage, traces of sensitive data may still persist within the model’s vectors.  Additionally, the NIH Genomic Data Sharing Policy considers AI models to be (still sensitive) derivatives of the data they train on;  in applying this interpretation, even methods that attempt to block certain outputs (e.g., via data masking  or response filtering ) cannot salvage the fact that the data may have been already improperly disclosed to, used by, and re-distributed by or as the model.

Some GenAI policies allow individuals to request that the company remove information about them, which is consistent with rules such as the HIPAA right for patients to request amendment.  However, companies also state they cannot guarantee such removal due the “technical capabilities” of the models.

While public GenAI policies and terms sometimes state input/output data will not be **sold** directly, if an AI model memorizes and leaks data or is considered a data derivative and is then sold as a commercial product, this could amount to selling the data which is often prohibited (Figure 2). Additionally, GenAI tools and companies often do not claim ownership over a user’s inputs and outputs but do state they own rights, title, and interest in their products and services, including models trained on such data.  

The LLMs that underly GenAI tools are trained on large amounts of unspecified public and proprietary datasets as well as other user inputs. With enough facts about research participants (e.g., their diagnosis, demographic and clinical information), model outputs could lead to **re-identification** (e.g., revealing [more] personal information about these participants), whether inadvertently or through explicit attacks.  LLMs are designed to determine relationships between words thus performing entity resolution such that it associates existing information it has already learned from model training with new information, whether that be inputted as prompts or new training data.  Therefore, re-identification could be possible with prompt-based strategies even when model training is disabled. 

GenAI tool policies and terms require that users take on a substantial amount of **responsibility** and **liability** especially with regard to ensuring they have appropriate rights and permission to use and provide (i.e., disclose) their data inputs, whether model training is enabled or disabled. This means that researchers are responsible for understanding whether and how the GenAI tool will handle the data according to their obligations and could be held accountable if something goes wrong. However, GenAI policies and terms are often convoluted, difficult to understand (e.g., use a variety of terms to describe input/output data, reference multiple documents that can be hard to follow), and change over time. Resources like this one can help educate the community on what terms and policies to look out for and what data protection rules to keep in mind. 

Additionally, researchers, repositories, and institutions may consider strategies that “free” some data from laws and rules relevant to biomedical data. For example, de-identifying data such that Common Rule or HIPAA no longer apply and determining that certain de-identified data are not sensitive or obtaining explicit consent such that it can be shared as **open (or unrestricted)** access instead of requiring controlled access, thereby allowing the data to be used in public GenAI tools. 

**These findings should be considered not only when using public GenAI tools but also when establishing enterprise agreements with GenAI companies (i.e., determining which provisions should or should not be included). They should also be considered when providing guidance to the research community regarding which data should or should not be used in a specific GenAI tool, whether public or private.**

<br/><br/>

# User Stories 
The following User Stories motivated and informed this Effort

| S#  | User Story | Current Problem | User Goal |
|----|----|----|-----|
|S74 | [As a researcher, I want to predict which participants in my study are most likely to benefit from a given drug based on their genetics (from whole genome sequencing), clinical records (from electronic health records), and other health information (from questionnaires)](https://github.com/NIH-NICHD-Ecosystem/UserStories/blob/main/stories/storyID-74.md) </li></ul> | I would like to enter the data about these participants into a public GenAI tool to jump-start my analysis, but I am not sure this is allowed| My goal is to understand how GenAI companies handle data input into their tools to determine whether this conflicts with legal or IRB requirements or what the participants agreed to in the consent form |
|S75 | [As a researcher, I want to use GenAI to run statistical analysis on genetic, clinical, and other health data from a controlled access data repository and generate graphs and other visuals ](https://github.com/NIH-NICHD-Ecosystem/UserStories/blob/main/stories/storyID-75.md)  </li></ul> | This requires entering the data into the tool, but I am not sure this is allowed| My goal is to understand how GenAI companies handle data input into their tools to determine whether this conflicts with the provisions of my data use agreement | 
|S76 | [As a repository curation team, I want to map submitted clinical data to a standard ontology (e.g., LOINC) using GenAI tools ](https://github.com/NIH-NICHD-Ecosystem/UserStories/blob/main/stories/storyID-76.md)  </li></ul> | The data, while de-identified, are sensitive human data that must be kept secure| My goal is to understand how GenAI companies handle data input into their tools to determine whether this conflicts with security requirements |
