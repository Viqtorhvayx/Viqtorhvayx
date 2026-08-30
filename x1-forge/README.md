# X1 Forge

The official developer starter kit for [X1 EcoChain](https://x1ecochain.gitbook.io/x1-ecochain-tech-whitepaper) — a low-energy, EVM-compatible Layer-1 running on physically distributed low-power nodes.

X1 Forge lowers the barrier for the next builder on X1 EcoChain: one command scaffolds a ready-to-deploy dApp, preconfigured for the Maculatus testnet, with wallet connect, a sample contract, and deploy/verify scripts already wired up.

## Quickstart

```bash
npx create-x1-app my-dapp
cd my-dapp
npm install
cp .env.example .env   # add your PRIVATE_KEY
npm run deploy:testnet
```

Check RPC health any time with:

```bash
npx create-x1-app status
```

Scaffold the ERC-20 starter instead of the default `Greeter` demo:

```bash
npx create-x1-app my-token --template erc20
```

See [`packages/create-x1-app`](./packages/create-x1-app) for the CLI, and `packages/create-x1-app/templates/` for what gets scaffolded (`default` and `erc20`).

## Project structure

```
x1-forge/
├── packages/
│   └── create-x1-app/       CLI that scaffolds new projects, plus `status` command
│       └── templates/
│           ├── default/     Hardhat + wallet-connect starter dApp
│           └── erc20/       OpenZeppelin ERC-20 starter with balance/transfer UI
├── docs/                    Quickstart & tutorials
└── GRANT_APPLICATION.md     X1 EcoChain Ecosystem Grants application draft
```

## Roadmap

- [x] **M1** — `create-x1-app` CLI + starter template (wallet connect, sample contract, deploy/verify scripts). Verified live: [`0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755`](https://maculatus-scan.x1eco.com/address/0xaF8ecc6741c26BCCc7ccCe9BfC1f2Cd73E8a2755)
- [x] **M2** — UX layer: one-click "Add to MetaMask", faucet instructions in CLI output, `status` command, second (ERC-20) template. Verified live: [`0xB41DB8E536DDb13670239577dd06d6e4bFEE9C53`](https://maculatus-scan.x1eco.com/address/0xB41DB8E536DDb13670239577dd06d6e4bFEE9C53)
- [ ] **M3** — Docs/tutorial site (quickstart, SDK guides, walkthrough video)
- [ ] **M4** — Reference dApp built end-to-end with the kit, deployed live

## Network reference

| | |
|---|---|
| Testnet | Maculatus |
| Chain ID | `10778` |
| RPC | `https://maculatus-rpc.x1eco.com/` |
| Explorer | `https://maculatus-scan.x1eco.com/` |
| Native token | `X1T` |
| Faucet | Discord `#faucet` channel — `/faucet <address>` |

## License

MIT
