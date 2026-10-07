---
layout: archive
permalink: /research/
title: "Research"
author_profile: true
---

{% include base_path %}

# 🔬 **Research** {#research}

My research aims to make the software supply chain safer and to understand how far AI can be trusted with security-critical software engineering tasks.

---

## 📄 **Publications under Review**

### Unveiling Malicious Logic: Towards a Statement-Level Taxonomy and Dataset for Securing Python Packages
👥 Ahmed Ryan, **Junaid Mansur Ifti**, Akond Ashfaque Ur Rahman, Md Erfan, Md Rayhanur Rahman  
📰 *Under review at IEEE Transactions on Software Engineering (TSE)* · 📚 6 citations

- Derived a fine-grained taxonomy of **47 malicious indicators** across **370 malicious Python packages**, enabling behavior-centric detection and training of semantic-aware models.
- Applied **sequential pattern mining** to uncover recurring indicator sequences that characterize common attack workflows, strengthening software supply-chain defenses.

---

## 🧪 **Ongoing Research**

### AutoSecuRe: Can an AI Agent Safely Fix Leaked Secrets?
*Automated Secret Migration and Benchmarking by LLM*  
📅 **June 2024 – Present** · 🔬 **Sole researcher**, designed and built from scratch · 🚧 *Unpublished, in progress*  
👨‍🏫 Supervised by **Dr. Md Rayhanur Rahman**, The University of Alabama

> **The question:** Security scanners can tell you *where* an API key or token leaked. They cannot fix it. If we hand that job to an LLM agent, how much should we trust the result?

**Why it matters.** Hard-coded credentials in version control have caused major real-world breaches, and detection tools stop at the alert. The real work comes after: provisioning a vault, rewriting the code, and not breaking anything. LLM agents can now edit whole repositories, but there is no rigorous way to tell a *correct* fix from one that merely silences the scanner.

**What I built.** An autonomous agent that completes the whole remediation loop:
1. 🔎 **Detect:** scans a repository, then uses an LLM audit step to tell real production secrets from harmless test credentials.
2. ☁️ **Migrate:** moves the real secrets into a secure vault (a local cloud mock in the research setting).
3. 🛠️ **Refactor:** rewrites the code to fetch secrets from the vault and adds the needed configuration.

**How it is judged.** Every fix is scored on three independent axes, so an agent cannot pass by gaming one of them:
- ✅ **Does it still work?** The project's own tests must keep passing.
- 🔐 **Is the secret really gone?** A follow-up scan must find nothing left in plaintext.
- 🌳 **Is it the right fix?** The code structure is compared with a human-verified solution, so shortcuts and hacks are penalized.

**Where it stands.** The methodology and an end-to-end proof of concept are done. I am now building a multi-language benchmark of vulnerable projects with expert solutions, which will be used to compare different LLMs head to head. Results will be shared once the work is published.

---

## 🎓 **Earlier Research**

### GAnomaly: ML-based Anomaly Detection for Google Analytics Traffic
📅 **2022** · Undergraduate Researcher, Distributed Systems & Software Engineering Research Group, University of Dhaka  
👨‍🏫 Supervised by **Dr. Kazi Muheymin-Us-Sakib**

- Built an ML-based web application combining statistical outlier detection and rule-based algorithms, based on the IEEE paper *“Using Google Analytics to Support Cybersecurity Forensics.”*
- [📂 Source code](https://github.com/bsse1027/SPL-3)

### Impact of Physical Health on Developer Productivity (GQM)
Goal–Question–Metric study with 48 software engineers in Bangladesh. [📄 Report](https://github.com/junaidmifti/GQM_Research/blob/main/Final%20Doc.pdf)

---

## 🤝 **References**
Available on request; listed on my [CV](/files/CV_junaid_mansur_ifti.pdf): Dr. Md Rayhanur Rahman (The University of Alabama), Dr. Kazi Muheymin-Us-Sakib and Dr. B M Mainul Hossain (University of Dhaka).
