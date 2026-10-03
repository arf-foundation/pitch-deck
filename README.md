# ARF AI Investor Deck — The Control Plane for Autonomous AI

This repository hosts the **non-confidential investor deck** for **ARF AI / Agentic Reliability Framework (ARF)**.

The current presentation is a **14-slide, 1920×1080 investor deck** positioning ARF as an execution-governance control plane between probabilistic agent intent and production state.

**Live deck:** [https://arf-foundation.github.io/pitch-deck/](https://arf-foundation.github.io/pitch-deck/)

**Deck status date:** October 3, 2026

---

## Important Note

The ARF **core engine, API control plane, gateway, and enterprise components are proprietary and access-controlled**. They are not open source and are not contained in this repository.

This repository contains non-confidential presentation material and presentation code only. Public access to the deck does not imply public access to the protected ARF runtime or enterprise implementation.

The deck also explicitly **does not claim patent protection**. Formal diligence is intended to distinguish company-owned software and methods, third-party dependencies, and any filed or registered intellectual property.

---

## Purpose

The deck is designed for investor and diligence conversations around:

- ARF's thesis that autonomous AI requires a **pre-execution governance layer**
- The architecture separating **candidate choice, safety gating, authorization, and execution**
- ARF's technical foundation: probabilistic risk reasoning feeding deterministic execution controls
- The initial market wedge and review-first commercialization strategy
- Current validation status, shipped capabilities, and near-term roadmap
- The pre-seed financing plan and path toward recurring platform revenue

---

## Deck Structure

The current `index.html` contains 14 slides:

1. **Title** — The Control Plane for Autonomous AI
2. **Problem** — AI is gaining the ability to act faster than enterprises can govern it
3. **Thesis** — Evaluate, Authorize, Recover, Prove
4. **Architecture** — Candidate generation/scoring, selection, gating, approval, and actuation
5. **Differentiation** — Probabilistic intelligence feeding deterministic execution governance
6. **Signed Intent** — Trusted authorization boundary using Ed25519-signed intent
7. **Defensibility** — Protected runtime, policy/risk layer, integrations, and accumulated governance knowledge
8. **Platform** — ARF as a standard control boundary for high-consequence autonomous systems
9. **Market Wedge** — Cloud infrastructure first, with financial services, healthcare, legal/compliance, and later expansion
10. **Business Model** — A free snapshot, a fixed-price write-access review, then a recurring continuous gate
11. **Status** — Current release line, test coverage, and validation status
12. **Roadmap** — Shipped capabilities vs. in-development enterprise work
13. **Financing** — Pre-seed raise and use of funds
14. **Next Step** — Technology, diligence, and investment discussion

---

## Product Positioning

ARF is presented as the control layer between agent intent and production execution.

The deck's core execution-governance model is:

- **Evaluate** — quantify risk, consequence, uncertainty, and evidence before release
- **Authorize** — apply deterministic policy, permissions, trusted signing, and autonomy boundaries
- **Recover** — treat reversibility and compensation as part of the decision
- **Prove** — retain an auditable record of the proposed action, selected action, decision basis, and execution outcome

The enterprise execution ladder shown in the deck includes:

- **Advisory** — governed recommendation without production authority
- **Supervised** — explicit approval boundary before execution
- **Autonomous** — execution only where policy, risk, trust, and recovery constraints allow it

A key invariant in the current architecture is that the **selected candidate is the same candidate described by the gates, approval requirements, audit records, and executor**.

---

## Technical Foundation

The investor deck currently highlights:

- **Bayesian risk fusion** — conjugate online updates, optional hierarchical shrinkage, and offline HMC prediction
- **Expected-loss minimization + CVaR** — approval, denial, and escalation decisions with the 95% CVaR tail used by default
- **Epistemic uncertainty** — bounded uncertainty combining hallucination, forecast uncertainty, and data sparsity, with Shapley attribution
- **Semantic memory** — FAISS-backed incident retrieval with learned or Bayesian memory weighting
- **Causal counterfactuals** — IPW and heterogeneous treatment-effect machinery
- **Formal verification** — TLA+ model checking plus property testing across Python and Rust for the permit/deny decision projection
- **AGSF online risk tracking**
- **Temporal drift detection**
- **Lyapunov stability monitoring**
- **Deterministic seeded sampling**
- **Immutable HealingIntent contract**

The signed-intent example in the deck uses **Ed25519** and a **SHA-256 context hash**.

---

## Market Wedge

The current deck starts commercialization where autonomous mistakes are expensive:

- **Cloud infrastructure** — configuration, remediation, incident response, deployments, and privileged operational actions
- **Financial services** — high-consequence workflows requiring authorization, risk controls, and traceability
- **Healthcare** — controlled workflows where uncertainty and governance requirements are material
- **Legal & compliance** — workflows where evidence, escalation, and auditability are part of the deliverable
- **Expansion** — energy, logistics, robotics, and other environments where software-driven decisions affect physical or economic state

The commercial wedge is **infrastructure-agent vendors moving from read-only to production writes, storage first**. A second track covers **agents that make regulated customer commitments** (lending, collections, refunds).

---

## Business Model

The current deck describes a review-first model with a path to recurring platform revenue:

- **Pilot snapshot:** free, for three founding teams, covering five named write tools from one agent, in exchange for a written reference
- **Write-access review:** **$4,500** fixed per agent. It covers every write path in the agreed tool inventory, mapped for reversibility and approval.
- **Continuous gate:** recurring, by invitation after a review. It is priced per engagement once a write path is modeled and validated.

The intended account progression is:

**Land a high-consequence workflow → controlled deployment → expand across more actions and agents → become a recurring production control-plane dependency.**

---

## Current Status

The deck reports the following current-state metrics and release information:

- **536** core tests passing in CI on each of Python 3.10, 3.11 and 3.12; 95 of the 117 pressure tests run on every push
- **772** enterprise tests passing in CI on each Python version, plus **113** Rust tests for the execution ladder
- Coverage across risk fusion, uncertainty, policy gating, signing, admission, approvals, reversibility, and the ONTAP admission proxy
- **Core v4.3.6**
- **Enterprise v4.3.6**
- **4.3.7**, the next release: its changes are merged and tested on main, and the version is not yet tagged

The enterprise layer is described as adding the execution boundary, trusted signing, candidate selection, and actuator integration around the protected core.

### Shipped / Current State

- Bayesian risk fusion + CVaR expected-loss decisioning
- Formal policy verification on the decision projection
- Enterprise trust anchor + Ed25519 intent signing
- Real candidate alternatives + per-candidate reversibility from live provider state
- No committed audit entry, no execution; one approval admits one attempt
- ONTAP MCP admission proxy, demonstrated on a simulated cluster

### In Development

- Live-cluster validation of the ONTAP write path
- Production execution for a first design partner (deployed, off by default)
- Customer-pulled audit exports for independent verification
- Broader production actuator coverage
- Repeatable enterprise pilots, contracts, and reference deployments

The deck states that the referenced core and enterprise repository state and CI were checked on **October 3, 2026**.

---

## Financing

The current investor deck presents:

- **$500K pre-seed raise**
- **$250K first close**

Planned use of capital includes:

- Product hardening
- Enterprise readiness
- Pilot conversion
- Distribution
- Execution capacity

Final securities terms, valuation/cap table, and allocation are reserved for formal fundraising diligence.

---

## Cited Cases in the Deck

The problem slide uses three cited examples to illustrate the execution-governance category:

- **Air Canada** — AI output becoming organizational liability
- **Cloudflare** — small configuration actions creating systemic impact
- **PocketOS** — excessive autonomy multiplying blast radius

These examples support the deck's thesis that governance must operate **before consequential execution**, not only through observability after failure.

---

## What's in This Repository

| File | Description |
|------|-------------|
| `index.html` | Self-contained packaged investor presentation with 14 animated 16:9 slides |
| `README.md` | Repository overview aligned with the current investor deck |
| `ARF - Primary Logo.png` | ARF primary logo asset |
| `ARF - Transparent Primary Logo.png` | Transparent ARF logo asset |
| `LICENSE` | Licensing terms for deck content and deck source code |
| `.nojekyll` | Ensures GitHub Pages serves the repository without Jekyll processing |
| `robots.txt` | Crawler directives for the published deck |

There is **no separate `SpeakerNotes.md` file in the current repository**.

---

## Presentation Controls

The deck runtime provides:

- Keyboard navigation with **← / → / ↑ / ↓**
- **Page Up / Page Down**
- **Space** to advance
- **Home / End**
- Number-key navigation
- **R** to reset to the first slide
- On touch devices, tapping the **left or right half** of the stage navigates backward or forward
- A bottom-center navigation overlay with slide count and controls
- A desktop thumbnail rail outside presentation mode
- Automatic scaling to fit the viewport
- Reduced-motion support via `prefers-reduced-motion`
- Browser printing with one slide per page for **Print → Save as PDF**

The current deck does **not** include the old 20-minute presentation timer or a separate speaker-notes document.

---

## Links

- **Live investor deck:** [https://arf-foundation.github.io/pitch-deck/](https://arf-foundation.github.io/pitch-deck/)
- **Public sandbox:** [https://www.arf-ai.com/#explore](https://www.arf-ai.com/#explore)
- **ARF GitHub organization:** [https://github.com/arf-foundation](https://github.com/arf-foundation)
- **ARF AI website:** [https://www.arf-ai.com](https://www.arf-ai.com)
- **Juan Petter on LinkedIn:** [https://www.linkedin.com/in/petterjuan/](https://www.linkedin.com/in/petterjuan/)
- **Contact:** [juan@arf-ai.com](mailto:juan@arf-ai.com)

---

## GitHub Pages

The deck is published from the repository root.

To deploy a fork:

1. Place `index.html` at the root of the default branch.
2. Open **Settings → Pages**.
3. Configure GitHub Pages to publish from the branch root.
4. Open the resulting GitHub Pages URL.

The bundled presentation is designed to run as a browser-based HTML deck and includes its presentation runtime and assets inside the packaged `index.html`.

---

## Search / Crawler Behavior

The current `index.html` declares:

`noindex, nofollow`

The repository's `robots.txt` also disallows crawling. The deck may be publicly reachable by URL while still being intentionally excluded from indexing.

---

## License

The repository license separates deck content, rendering code, and ARF software:

- **Deck content** — text, narrative, slides, diagrams, and images are © ARF Foundation, all rights reserved; viewing and linking are permitted, but copying, redistribution, adaptation, and derivative works require permission
- **Deck source code** — the HTML, CSS, and JavaScript that render `index.html` are licensed under **Apache License 2.0**
- **ARF software** — the core engine, API control plane, gateway, and enterprise components remain proprietary, access-controlled, and outside the scope of this repository's license

See [LICENSE](LICENSE) for the governing terms.

---

## Contact

For investor discussions, technical diligence, enterprise deployment conversations, or partnership inquiries:

**Juan Petter**  
Founder, ARF AI  
[juan@arf-ai.com](mailto:juan@arf-ai.com)  
[https://www.arf-ai.com](https://www.arf-ai.com)

---

*README aligned with the current `index.html` investor deck. Deck content current as of October 3, 2026.*
