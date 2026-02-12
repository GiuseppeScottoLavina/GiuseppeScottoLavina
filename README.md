### Hi, I'm Giuseppe 👋
# Exploring the AI-First Developer Experience.

> **In 2010, "Mobile-First" changed *how* we build software.**
> **In 2026, the question is: *who* are we building it for?**

I'm a Senior Full Stack Developer exploring a specific, uncomfortable question:

> **What happens when we design development infrastructure assuming
> an AI Agent is a first-class consumer — not just as autocomplete,
> but as an autonomous collaborator?**

Current frameworks and tools were designed for human developers. They work.
But they create friction for Agents: implicit behaviors cause hallucinations,
unvetted dependencies create security risks, and documentation requires
probabilistic interpretation rather than deterministic inspection.

I don't have the definitive answers yet. I have **experiments**.

---

## 🧪 Open Source Experiments (PoCs)

The industry trend is to solve Agent friction by scaling compute
(multimodal vision, infinite context windows).
I'm stress-testing a complementary approach: making tools deterministic
so the Agent doesn't need to guess.

| The Friction | The Experiment | The Engineering Challenge |
| :--- | :--- | :--- |
| **Agents hallucinate UI APIs** | [**AgentUI**](https://github.com/GiuseppeScottoLavina/AgentUI)<br>*(Web Components with `.describe()`)* | **Introspection vs Documentation.** <br>*Challenge: Automating metadata generation (e.g., via AST) to avoid manually writing `.describe()` and violating the DRY principle.* |
| **Agents install unvetted packages** | [**AgentRegistry**](https://github.com/GiuseppeScottoLavina/AgentRegistry)<br>*(Local NPM proxy & firewall)* | **Guardrails before Trust.** Scanning for prompt injections pre-install.<br>*Challenge: Reducing false positives without killing agent autonomy.* |
| **Agents lack cross-context state** | [**CrossBus**](https://github.com/GiuseppeScottoLavina/CrossBus)<br>*(Unified Messaging)* | **Predictable coordination.** A seamless communication layer across tabs, workers, and servers.<br>*Challenge: Maintaining deterministic state sync without massive performance overhead.* |

---

## 🔬 Hypotheses I'm Testing

These are hypotheses, not conclusions. The code exists to prove or disprove them.

1. **Introspection outperforms Probabilistic Vision** — Modern Agents *can* read screens, but visual inference is token-heavy and probabilistic. Runtime DOM introspection (`.describe()`) is lightweight and deterministic.
2. **Explicit beats Implicit** — "Magic" behaviors that save keystrokes for humans (auto-imports, implicit states) confuse probabilistic systems. Explicit boundaries reduce LLM errors.
3. **Infrastructure safety outperforms prompt safety** — You cannot secure an Agent purely by telling it "don't install malware". Safety must be enforced at the infrastructure level.

---

## 📊 What I'm Working On Next

These are early-stage PoCs, not products. To validate or disprove these hypotheses,
my current focus is:

- **Comparative benchmarks:** Token cost and code accuracy of `.describe()` versus standard Docs + RAG.
- **False-positive tuning:** Calibrating `AgentRegistry` to be secure but usable in daily workflows.

If the data shows these ideas don't work, I'll document why and pivot.

But if you're exploring the Agentic workflow space, or if you think this
deterministic approach is fundamentally flawed and brute-force scaling will win,
**I want to hear from you.**

I build in public to be proven wrong. Let's connect.

---

<p align="left">
  <a href="https://github.com/GiuseppeScottoLavina?tab=repositories">
    <img src="https://img.shields.io/badge/Check_my_experiments-black?style=for-the-badge&logo=github" alt="Repos" />
  </a>
</p>
