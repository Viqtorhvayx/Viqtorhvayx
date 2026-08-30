# X1 EcoChain Ecosystem Grants — Application Draft

Draft answers for the [X1 EcoChain Grant Program Application Form](https://airtable.com/appMvL5KlSmE9J3I4/paglccI2kQaFErlF3/form). Fill in the bracketed `[ ]` fields before submitting.

---

**Project Name**
X1 Forge

**Project Type**
Developer Tooling / Infrastructure

**Project Abstract and Objective**
X1 Forge is the official developer starter kit for X1 EcoChain: a single CLI command (`npx create-x1-app`) that scaffolds a ready-to-deploy EVM dApp preconfigured for the Maculatus testnet — sample contract, Hardhat deploy/verify scripts, and a wallet-connect frontend with a one-click "Add X1 EcoChain to MetaMask" flow, all wired up out of the box. The primary objective is lowering the time-to-first-deploy for new builders on X1 EcoChain from hours of manually assembling RPC config, network params, and boilerplate to under five minutes. Key use cases: hackathon participants who need a working base fast, teams evaluating X1 EcoChain who want to test-drive it without reading the full docs first, and existing X1 EcoChain projects who want a maintained reference implementation to fork. This directly enhances developer tools (the CLI, template, docs) and user experience (the in-browser network-add flow, faucet guidance) — the two things this grant program is designed to fund — and is well-suited to emerging market conditions because it removes cost/expertise barriers for builders who don't have the time to reverse-engineer chain config from scattered docs.

**Technical Roadmap**
- M1 (Weeks 1–2): `create-x1-app` CLI + default template — Hardhat project preconfigured with Maculatus testnet (chain ID 10778), sample `Greeter` contract, deploy + test scripts, wallet-connect frontend demo. **[Status: complete — CLI scaffolds, `npm test` and `hardhat compile` pass, and a contract deployed live to the Maculatus testnet: [`0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755`](https://maculatus-scan.x1eco.com/address/0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755).]**
- M2 (Weeks 3–4): UX layer — one-click "Add to MetaMask" (implemented), CLI output with faucet instructions (implemented), a network-status check command, and a second template (e.g. ERC-20 or NFT starter).
- M3 (Weeks 5–6): Docs/tutorial site — quickstart, SDK integration guides (JS + Python), a short walkthrough video, published to a docs domain.
- M4 (Weeks 7–8): Reference dApp built end-to-end with the kit, deployed live on the Maculatus testnet, linked from the docs as a worked example.

**Project website**
[URL — e.g. GitHub Pages or docs site once M3 ships]

**Project X (Twitter)**
[@handle]

**Previous Funding**
None

**Funding Details**
N/A

**Requested Funding Range**
[Select the range closest to your total ask — see Grant Budget Structure below]

**Grant Budget Structure & Milestones**

Requesting an upfront payment (up to 20%) to cover initial development, with the remainder released against the four milestones below.

- **Milestone 1**
  - Name: CLI + Starter Template
  - Description: Build and publish `create-x1-app`, a CLI that scaffolds a Hardhat-based dApp preconfigured for the Maculatus testnet, with a sample contract, deploy/test scripts, and a wallet-connect frontend demo.
  - Deliverables & Success Metrics/KPIs: CLI published to npm; running `npx create-x1-app <name>` produces a project where `npm test` and `npm run deploy:testnet` succeed against the live testnet; public GitHub repo. **Already demonstrated: a contract scaffolded and deployed via this exact pipeline is live at `0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755` on the Maculatus testnet.**
  - Estimated Completion Date: [date]
  - Amount Requested: [amount]

- **Milestone 2**
  - Name: UX Layer
  - Description: Add one-click network setup, CLI-embedded faucet guidance, a network-status check, and a second starter template (ERC-20 or NFT).
  - Deliverables & Success Metrics/KPIs: `wallet_addEthereumChain` flow ships in the frontend demo; `create-x1-app --template <name>` supports 2+ templates; network status command returns live RPC health.
  - Estimated Completion Date: [date]
  - Amount Requested: [amount]

- **Milestone 3**
  - Name: Docs & Tutorials
  - Description: Publish a quickstart, JS/Python SDK integration guides, and a short walkthrough video.
  - Deliverables & Success Metrics/KPIs: Docs site live at [domain]; at least 3 guides published; video published and linked from the docs and README.
  - Estimated Completion Date: [date]
  - Amount Requested: [amount]

- **Milestone 4**
  - Name: Reference dApp
  - Description: Ship a complete example application built with X1 Forge, deployed live on the Maculatus testnet.
  - Deliverables & Success Metrics/KPIs: Contract verified on the X1 EcoChain explorer; live frontend URL; linked as the canonical example from the docs.
  - Estimated Completion Date: [date]
  - Amount Requested: [amount]

**Current Development Stage**
Milestone 1 complete — CLI and default template built and verified end-to-end against the live Maculatus testnet: scaffold, install, compile, test, and deploy all succeed, with a deployed sample contract at [`0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755`](https://maculatus-scan.x1eco.com/address/0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755).

**Duration working on the project**
[e.g. "2 weeks" — fill in actual]

**Project live status**
Not yet live — pre-launch / in development

---

**Applicant Full Name**
[Your name]

**Applicant Email**
victorolagbaye679@gmail.com

**Applicant Job Title**
[e.g. Founder / Solo Developer]

**Applicant Bio**
[2–3 sentences: background, relevant experience, prior projects shipped]

**Telegram**
[@handle]

**Team size**
[e.g. 1 (solo)]

**How did you hear about Grant Program?**
[e.g. X1 EcoChain documentation / Discord / Twitter]

**Are there other details, milestones, or contributions you'd like to highlight?**
X1 Forge is designed to be a maintained public good, not a one-off deliverable — the plan is to keep the CLI and templates updated as X1 EcoChain's tooling evolves (SDK changes, mainnet launch, new EVM features), and to accept community template contributions once the base kit ships.

---

## Notes for the applicant (not part of the form)

- Fill in every `[ ]` before submitting — funding amounts, dates, and personal details are yours to set.
- The CLI and M1 template already exist in this repo (`x1-forge/`) and have been verified fully end-to-end: `create-x1-app` scaffolds correctly, `npm test` passes, `hardhat compile` succeeds against Solidity 0.8.24, and a real deploy to the live Maculatus testnet succeeded (`0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755`). The wallet used was generated fresh for this test and funded via the Discord faucet — treat it as disposable; use your own wallet for the actual submission/demo if you want continued control of it.
- Consider publishing the repo publicly and linking it in "Project website" before submitting — reviewers will likely check for a real, inspectable codebase.
