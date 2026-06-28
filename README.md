# LLM Security Research
**Researcher:** Ajay Kalbhile | SOC Analyst | Penetration Tester
**Location:** Pune, India
**Contact:** ajaykalbhile31@gmail.com
**LinkedIn:** linkedin.com/in/ajaykalbhile

---

## About This Project
Hands-on security research into Large Language Model (LLM) 
vulnerabilities. Covers real prompt injection testing, OWASP LLM 
Top 10 analysis, and AI red teaming methodology.

This research demonstrates practical AI security skills directly 
applicable to securing enterprise AI deployments.

---

## Research Areas

### Prompt Injection Testing — Gandalf AI
6/8 levels completed on Lakera's Gandalf AI security challenge.
Successfully bypassed progressive AI defenses using:
- Fictional framing
- Character encoding bypass
- Language translation (Pig Latin)
- Sentence completion injection
- Metaphorical extraction

[Full findings → gandalf-labs/findings.md]

### OWASP LLM Top 10 Coverage
- ✅ LLM01 Prompt Injection
- ✅ LLM02 Insecure Output Handling  
- ✅ LLM05 Supply Chain Vulnerabilities
- ✅ LLM06 Sensitive Information Disclosure
- ✅ LLM07 Insecure Plugin Design

---

## Skills Demonstrated
- AI/LLM vulnerability assessment
- Prompt injection attack methodology
- OWASP LLM Top 10 framework application
- Security research documentation
- Defensive recommendation development

---

## Tools & Platforms
- Gandalf AI (Lakera) — prompt injection practice
- OWASP LLM Top 10 framework
- Garak LLM scanner (in progress)
## Screenshots — Proof of Research

### Level 1 — Direct Extraction (No Defense)
![Level 1](gandalf-labs/screenshots/level1-cocoloco.png)

### Level 2 — Fictional Framing Bypass
![Level 2](gandalf-labs/screenshots/level2-potential.png)

### Level 3 — Character Encoding Bypass
![Level 3](gandalf-labs/screenshots/level3-wavelength.png)

### Level 4 — Language Translation Bypass
![Level 4](gandalf-labs/screenshots/level4-underground.png)

### Level 5 — Sentence Completion Injection
![Level 5](gandalf-labs/screenshots/level5-bestowed.png)

### Level 6 — Metaphorical Extraction
![Level 6](gandalf-labs/screenshots/level6-underpass.png)
---


## References
- OWASP LLM Top 10: owasp.org/www-project-top-10-for-large-language-model-applications
- Gandalf AI: gandalf.lakera.ai
- Garak: github.com/NVIDIA/garak

## Garak Full Scan Results — GPT-2

**Date:** June 28, 2026
**Tool:** Garak v0.15.1
**Target:** huggingface:gpt2
**Overall Security Score:** 78% (DC-3 Risk Level)

| Probe | Pass Rate | Attack Success Rate | Severity |
|---|---|---|---|
| HijackHateHumans | 82.11% | 17.89% | Medium |
| HijackKillHumans | 74.06% | **25.94%** | High |
| HijackLongPrompt | 88.44% | 11.56% | Medium |

**Critical Finding:** HijackKillHumans probe achieved
25.94% attack success rate — meaning 1 in 4 violent
content injection attempts succeeded against GPT-2.

**OWASP Mapping:** LLM01 — Prompt Injection
**DEFCON Level:** DC-3 (Medium Risk)
**Recommendation:** Safety fine-tuning (RLHF), output
filtering, and input sanitization required before
production deployment.
