---
layout: archive
permalink: /research/
title: "Research"
author_profile: true
---

{% include base_path %}

# 🔬 **Research** {#research}

My research aims to automate more of software engineering with AI, and to understand how far it can be trusted. My current work applies this to software security: making the software supply chain safer and testing LLMs on security-critical tasks. I am keen to extend it to automated testing and other AI-driven SE tasks.

---

## 📄 **Publications under Review**

### Between the Lines: A Statement-Level Annotated Dataset and Behavioral Taxonomy for Malicious Python Packages
👥 Ahmed Ryan, **Junaid Mansur Ifti**, Md Erfan, Akond Ashfaque Ur Rahman, [Md Rayhanur Rahman](https://eng.ua.edu/eng-directory/dr-md-rayhanur-rahman/)  
📅 **2026** · 📰 *Under review at IEEE Transactions on Software Engineering (TSE)* · 🤝 Collaboration with researchers at **The University of Alabama** and **Auburn University** · 📚 6 citations  
🔗 [📄 Read the preprint on arXiv](https://arxiv.org/pdf/2512.12559) · [arXiv abstract page](https://arxiv.org/abs/2512.12559)

Existing malicious-package datasets only say *whether* a package is malicious, not *which statements* make it so. This work shifts analysis from binary classification to explainable, behavior-centric detection.

- **Dataset:** statement-level annotations for **370 malicious Python packages** (833 files, 90,527 lines of code) with **2,962 labeled occurrences** of malicious behavior.
- **Taxonomy:** **47 malicious indicators across 7 types** (e.g., execution, exfiltration, defense evasion, network operations).
- **LLM detection:** injecting the taxonomy into prompts improves detection **precision by 9% on average**, which directly reduces false positives.
- **Attack workflows:** **sequential pattern mining** reveals recurring indicator sequences that characterize common attack chains, giving heuristics for supply-chain defenses.

---

## 🧪 **Ongoing Research**

### AutoSecuRe: Can an AI Agent Safely Fix Leaked Secrets?
*Automated Secret Migration and Benchmarking by LLM*  
📅 **February 2026 – Present** · 🔬 **Sole researcher**, designed and built from scratch · 🚧 *Unpublished, in progress*  
👨‍🏫 Supervised by **[Dr. Md Rayhanur Rahman](https://eng.ua.edu/eng-directory/dr-md-rayhanur-rahman/)**, The University of Alabama

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
📅 **2022** · Undergraduate Researcher, [Distributed Systems & Software Engineering Research Group](https://dsse.iit.du.ac.bd/), University of Dhaka  
👨‍🏫 Supervised by **Dr. Kazi Muheymin-Us-Sakib**

- Built an ML-based web application combining statistical outlier detection and rule-based algorithms, based on the IEEE paper *“Using Google Analytics to Support Cybersecurity Forensics.”*
- [📂 Source code](https://github.com/bsse1027/SPL-3)

### Impact of Physical Health on Developer Productivity (GQM)
Goal–Question–Metric study with 48 software engineers in Bangladesh. [📄 Report](https://github.com/junaidmifti/GQM_Research/blob/main/Final%20Doc.pdf)

---

## 🤝 **References**
Available on request; listed on my [CV](/files/CV_junaid_mansur_ifti.pdf): [Dr. Md Rayhanur Rahman](https://eng.ua.edu/eng-directory/dr-md-rayhanur-rahman/) (The University of Alabama), Dr. Kazi Muheymin-Us-Sakib and Dr. B M Mainul Hossain (University of Dhaka).
