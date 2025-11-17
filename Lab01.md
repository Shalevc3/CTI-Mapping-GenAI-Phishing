# Lab 01: Mapping Cyber Threat & Attacks

## 🔗 Sources
- **Unit 42 – Palo Alto Networks:** *Fashionable Phishing Bait: GenAI on the Hook (2025)*

---

## 📝 Description and Schema

Threat actors are exploiting Generative AI (GenAI) platforms to quickly create and publish phishing pages. Using AI-powered website builders and writing assistants, attackers can generate realistic, brand-like websites within seconds and host them on legitimate services with no verification. This greatly increases the scale and efficiency of phishing operations.

Victims are often lured through AI-generated buttons such as “View Document” or “Show Coupon,” which redirect them to attacker-controlled credential harvesting pages.

The attack pattern typically involves:

1. Rapidly generating phishing sites using AI website builders.  
2. Mimicking trusted brands with AI-generated text and images.  
3. Hosting malicious content on legitimate AI/SaaS platforms.  
4. Redirecting victims to credential theft pages.  
5. Automating large-scale deployment using low-code AI tools.

---

## 🛡️ Attribution to Tactic/Technique

| Attribution to Tactic/Technique | Tactic / Technique / Sub-Technique | Title | MITRE ATT&CK ID | Use |
|---|---|---|---|---|
| Initial Access | Phishing → Spearphishing Link | AI-generated phishing pages & links created via website builders | T1566.002 | Redirects victims to credential theft pages using AI-generated links |
| Initial Access | Phishing | AI-generated text used to craft convincing phishing messages | T1566 | Writing assistants & chatbots generate realistic social-engineering content |
| Initial Access | User Execution → Malicious Link | Victims clicking “View Document” / “Show Coupon” | T1204.001 | Executes attacker-controlled phishing pages hosted on AI platforms |
| Resource Development | Develop Capabilities → Malicious Websites | Attackers generate phishing sites using AI website builders | T1587.006 | Rapid creation of full phishing sites with cloned branding |
| Resource Development | Acquire Infrastructure → Web Services | Abuse of legitimate AI/SaaS platforms for hosting phishing content | T1583.006 | Hosting phishing pages on trusted AI platforms to evade detection |
| Defense Evasion | Masquerading | AI-generated sites impersonate legitimate brands | T1036 | Phishing sites appear authentic due to AI-generated text and images |
| Collection | Credentials from Web Services | Credential harvesting after phishing redirect | T1056.003 | Redirects victims to fake login pages to capture credentials |
| Command & Control | Web Services | Leveraging legitimate AI/SaaS platforms as staging points | T1102 | Using trusted platforms as delivery and hosting channels |
| Impact / Exfiltration | Exfiltration Over Web Services | Exfiltration of stolen credentials through hosted pages | T1567 | Credentials exfiltrated through AI-generated phishing sites |

