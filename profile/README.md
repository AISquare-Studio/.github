<!-- Hero Banner -->
<div align="center">
  <picture>
    <img src="https://github.com/user-attachments/assets/30768baf-55a3-4af7-9622-d9398c2f62b7" width="100%" style="border-radius: 12px;" alt="AISquare Studio — AI governance and trust infrastructure" />
  </picture>
</div>

<br/>

<div align="center">

  <!-- Badges -->
  <a href="https://aisquare.studio"><img src="https://img.shields.io/badge/Website-aisquare.studio-0d9488?style=for-the-badge&logo=globe&logoColor=white" alt="Website" /></a>
  <a href="https://docs.aisquare.studio"><img src="https://img.shields.io/badge/Docs-docs.aisquare.studio-2563eb?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Docs" /></a>
  <a href="https://github.com/AISquare-Studio"><img src="https://img.shields.io/badge/Open_Source-Apache_2.0-f0883e?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="Open Source" /></a>
  <a href="https://feedback.aisquare.studio"><img src="https://img.shields.io/badge/Feedback-Share_Ideas-7c3aed?style=for-the-badge&logo=git-extensions&logoColor=white" alt="Feedback" /></a>

</div>

<br/>

## 🔷 About Us

**AISquare Studio** builds the **governance layer for AI agents**. We create open-source tools that record _why_ AI decisions are made, enforce policies on what agents can do, and give humans structured workflows to review, approve, or intervene — without replacing your existing agent framework.

> Think of us as the system of record for AI decisions, the same way financial systems track transactions.  
> Except the transactions are *"the AI decided to email your CEO at 3 AM."*

<br/>

---

## 🏗️ What We're Building

<!-- AI Extends You — product showcase -->
<div align="center">
  <picture>
    <img src="https://github.com/user-attachments/assets/96e9e4aa-9481-426e-9bb8-4e67628a3106" width="100%" style="border-radius: 12px;" alt="AI Extends You. It Never Replaces You — Book Appointments, Play Live Challenges, Connect Personally" />
  </picture>
</div>

<br/>

<table>
  <tr>
    <td width="50%" valign="top">
      <h3 align="center">🛡️ Governance & Audit</h3>
      <p align="center">Full decision audit trails for AI agents — every action logged, every policy enforced, every override documented.</p>
    </td>
    <td width="50%" valign="top">
      <h3 align="center">🧪 Automated QA</h3>
      <p align="center">Turn plain-English test descriptions into real Playwright tests — powered by AI, triggered from your PRs.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3 align="center">⚙️ Agent Orchestration</h3>
      <p align="center">Django-native framework for agentic workflows — DB-based job management, YAML pipelines, real-time event streaming.</p>
    </td>
    <td width="50%" valign="top">
      <h3 align="center">🔌 SDK & Integrations</h3>
      <p align="center">Client libraries and adapters for LangChain, CrewAI, AutoGen — plug governance into your existing stack.</p>
    </td>
  </tr>
</table>

<br/>

---

## 📦 Our Repositories

<p align="center">Click on a card to explore the project. ⭐ Star your favorites to show support!</p>

<!-- Row 1: Flagship repos -->
<div align="center">
  <a href="https://github.com/AISquare-Studio/AISquare-Studio-QA">
    <img src="pin-aisquare-studio-qa.svg" alt="AISquare-Studio-QA" />
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com/AISquare-Studio/awesome-aisquare">
    <img src="pin-awesome-aisquare.svg" alt="awesome-aisquare" />
  </a>
</div>

<br/>

<!-- Row 2: More repos -->
<div align="center">
  <a href="https://github.com/AISquare-Studio/django-ais">
    <img src="pin-django-ais.svg" alt="django-ais" />
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com/AISquare-Studio/aisquare">
    <img src="pin-aisquare-sdk.svg" alt="aisquare SDK" />
  </a>
</div>

<br/>

<!-- Row 3 -->
<div align="center">
  <a href="https://github.com/AISquare-Studio/Opengrowth-Website">
    <img src="pin-opengrowth-website.svg" alt="Opengrowth-Website" />
  </a>
</div>

<br/>

---

## 🧩 How the Pieces Fit Together

```
┌─────────────────────┐     ┌────────────────────────┐     ┌───────────────────────┐
│     Your Agent      │────▶│   AISquare Governance  │────▶│       AutoQA          │
│  (any framework)    │     │   (audit + policy)     │     │  (test generation)    │
└─────────────────────┘     └────────────────────────┘     └───────────────────────┘
                                       │
                                       ▼
                            ┌────────────────────────┐
                            │      django-ais        │
                            │   (orchestration)      │
                            └────────────────────────┘
                                       │
                                       ▼
                            ┌────────────────────────┐
                            │    AISquare SDK        │
                            │  (client libraries)    │
                            └────────────────────────┘
```

Your agent framework handles reasoning. **AISquare handles the *"wait, should you actually do that?"* part** — recording decisions, enforcing policies, and routing to human review. **AutoQA** validates behavior through generated tests. **django-ais** orchestrates multi-step workflows inside Django.

<br/>

<!-- Platform visual -->
<div align="center">
  <picture>
    <img src="https://github.com/user-attachments/assets/4cfa262d-fb26-4102-a1be-1c24f3aaf37e" width="100%" style="border-radius: 12px;" alt="AISquare Studio platform" />
  </picture>
</div>

<br/>

---

## ⚡ Quick Start

### AutoQA — AI-powered test generation in your PRs

```yaml
# .github/workflows/autoqa.yml
name: AutoQA
on:
  pull_request:
    types: [opened, edited, synchronize]

jobs:
  autoqa:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: AISquare-Studio/AISquare-Studio-QA@main
        with:
          openai_api_key: ${{ secrets.OPENAI_API_KEY }}
          staging_url: ${{ secrets.STAGING_URL }}
          mode: generate
```

Write tests in plain English inside your PR body, and AutoQA turns them into real Playwright tests. ✨

<br/>

### django-ais — agentic workflows in Django

```bash
pip install django-ais
```

```python
from django_ais import Worker

class SummaryWorker(Worker):
    name = "summarizer"

    def execute(self, job):
        return {"summary": summarize(job.payload["text"])}
```

Define workflows in YAML, stream events over SSE/WebSocket, and manage jobs through the Django ORM.

<br/>

---

## 🗺️ Roadmap

<p align="center">
  💡 Click on a card to explore the task progress<br/>
  🤝 Your reactions guide development! Add a ❤️ to your favorite features
</p>

<!-- Status summary -->
<div align="center">
<table>
<tr>
<td align="center"><img src="https://img.shields.io/badge/💡_idea-8b5cf6?style=flat-square" alt="idea" /><br/><h3>2</h3></td>
<td align="center"><img src="https://img.shields.io/badge/📋_planned-3b82f6?style=flat-square" alt="planned" /><br/><h3>2</h3></td>
<td align="center"><img src="https://img.shields.io/badge/🔨_in_progress-f59e0b?style=flat-square" alt="in progress" /><br/><h3>1</h3></td>
<td align="center"><img src="https://img.shields.io/badge/✅_done-22c55e?style=flat-square" alt="done" /><br/><h3>4</h3></td>
</tr>
</table>
</div>

<!-- Roadmap cards -->
<table width="100%">

<tr><td>
<h4>🟢 <a href="https://github.com/AISquare-Studio/AISquare-Studio-QA">AutoQA GitHub Action</a></h4>
<img src="https://img.shields.io/badge/status:done-22c55e?style=flat-square" alt="status:done" />
<img src="https://img.shields.io/badge/prio:high-ef4444?style=flat-square" alt="prio:high" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
🟩🟩🟩🟩🟩🟩🟩🟩🟩🟩 <b>100%</b> complete<br/>
<sub>AI-powered test generation from PR descriptions</sub>
</td></tr>

<tr><td>
<h4>🟢 <a href="https://github.com/AISquare-Studio/django-ais">django-ais</a></h4>
<img src="https://img.shields.io/badge/status:done-22c55e?style=flat-square" alt="status:done" />
<img src="https://img.shields.io/badge/prio:high-ef4444?style=flat-square" alt="prio:high" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
🟩🟩🟩🟩🟩🟩🟩🟩🟩🟩 <b>100%</b> complete<br/>
<sub>Django-native orchestration for agentic workflows</sub>
</td></tr>

<tr><td>
<h4>🟢 <a href="https://github.com/AISquare-Studio/awesome-aisquare">awesome-aisquare</a></h4>
<img src="https://img.shields.io/badge/status:done-22c55e?style=flat-square" alt="status:done" />
<img src="https://img.shields.io/badge/prio:medium-f97316?style=flat-square" alt="prio:medium" />
<img src="https://img.shields.io/badge/type:docs-16a34a?style=flat-square" alt="type:docs" /><br/>
🟩🟩🟩🟩🟩🟩🟩🟩🟩🟩 <b>100%</b> complete<br/>
<sub>Ecosystem hub with quickstarts and documentation</sub>
</td></tr>

<tr><td>
<h4>🟢 <a href="https://github.com/AISquare-Studio/aisquare">AISquare SDK</a></h4>
<img src="https://img.shields.io/badge/status:done-22c55e?style=flat-square" alt="status:done" />
<img src="https://img.shields.io/badge/prio:high-ef4444?style=flat-square" alt="prio:high" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
🟩🟩🟩🟩🟩🟩🟩🟩🟩🟩 <b>100%</b> complete<br/>
<sub>Client libraries for direct API integration</sub>
</td></tr>

<tr><td>
<h4>🟡 aisquare-examples</h4>
<img src="https://img.shields.io/badge/status:in_progress-f59e0b?style=flat-square" alt="status:in_progress" />
<img src="https://img.shields.io/badge/prio:medium-f97316?style=flat-square" alt="prio:medium" />
<img src="https://img.shields.io/badge/type:docs-16a34a?style=flat-square" alt="type:docs" /><br/>
🟩🟩🟩⬜⬜⬜⬜⬜⬜⬜ <b>30%</b> complete · 3 done · 7 to do<br/>
<sub>Runnable governance scenario examples</sub>
</td></tr>

<tr><td>
<h4>🔵 aisquare-templates</h4>
<img src="https://img.shields.io/badge/status:planned-3b82f6?style=flat-square" alt="status:planned" />
<img src="https://img.shields.io/badge/prio:medium-f97316?style=flat-square" alt="prio:medium" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ <b>0%</b> complete<br/>
<sub>Starter scaffolds for governed AI apps</sub>
</td></tr>

<tr><td>
<h4>🔵 aisquare-integrations</h4>
<img src="https://img.shields.io/badge/status:planned-3b82f6?style=flat-square" alt="status:planned" />
<img src="https://img.shields.io/badge/prio:high-ef4444?style=flat-square" alt="prio:high" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ <b>0%</b> complete<br/>
<sub>Adapters for LangChain, CrewAI, AutoGen</sub>
</td></tr>

<tr><td>
<h4>🟣 Dashboard</h4>
<img src="https://img.shields.io/badge/status:idea-8b5cf6?style=flat-square" alt="status:idea" />
<img src="https://img.shields.io/badge/prio:high-ef4444?style=flat-square" alt="prio:high" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
<sub>Visual interface for audit trail exploration</sub>
</td></tr>

<tr><td>
<h4>🟣 Policy Engine v2</h4>
<img src="https://img.shields.io/badge/status:idea-8b5cf6?style=flat-square" alt="status:idea" />
<img src="https://img.shields.io/badge/prio:high-ef4444?style=flat-square" alt="prio:high" />
<img src="https://img.shields.io/badge/type:feat-3b82f6?style=flat-square" alt="type:feat" /><br/>
<sub>Advanced rule builder for agent constraints</sub>
</td></tr>

</table>

<br/>

---

## 🤝 Get Involved

<!-- Community visual -->
<div align="center">
  <picture>
    <img src="https://github.com/user-attachments/assets/38ecea0c-684b-486a-85db-95da2d10a84e" width="100%" style="border-radius: 12px;" alt="AISquare Studio community and collaboration" />
  </picture>
</div>

<br/>

<div align="center">

  <a href="https://github.com/AISquare-Studio/awesome-aisquare/blob/main/CONTRIBUTING.md"><img src="https://img.shields.io/badge/🤝_Contributing-Guidelines-16a34a?style=for-the-badge" alt="Contributing" /></a>
  <a href="https://github.com/orgs/AISquare-Studio/discussions"><img src="https://img.shields.io/badge/💬_Discussions-Join_Us-58a6ff?style=for-the-badge" alt="Discussions" /></a>
  <a href="https://feedback.aisquare.studio"><img src="https://img.shields.io/badge/💡_Feedback-Share_Ideas-ea580c?style=for-the-badge" alt="Feedback" /></a>

</div>

<br/>

We welcome contributions across the entire ecosystem! Look for issues tagged **"good first issue"** across any of our repos — it's the perfect entry point.

<br/>

---

## 📬 Community & Support

| Channel | Link |
|:--------|:-----|
| 📖 **Documentation** | [docs.aisquare.studio](https://docs.aisquare.studio) |
| 🔌 **API Reference** | [docs.aisquare.studio/api-reference](https://docs.aisquare.studio/api-reference) |
| 🌐 **Website** | [aisquare.studio](https://aisquare.studio) |
| 💬 **Discussions** | [GitHub Discussions](https://github.com/orgs/AISquare-Studio/discussions) |
| 💡 **Feedback** | [feedback.aisquare.studio](https://feedback.aisquare.studio) |
| 🔒 **Security** | [Responsible Disclosure](https://github.com/AISquare-Studio/awesome-aisquare/blob/main/SECURITY.md) |
| ✉️ **Email** | [bots@aisquare.com](mailto:bots@aisquare.com) |

<br/>

---

<div align="center">

  <sub>Built with ❤️ by the <b>AISquare Studio</b> team — because your AI agents deserve accountability.</sub>

  <br/><br/>

  <a href="https://github.com/AISquare-Studio"><img src="https://img.shields.io/badge/AISquare_Studio-Follow_Us-0d1117?style=flat-square&logo=github&logoColor=white" alt="Follow Us" /></a>

</div>
