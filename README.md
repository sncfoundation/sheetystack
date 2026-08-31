<p align="center">
  <img src="https://sncfoundation.github.io/logos/sheetystack.svg" width="96" alt="SheetyStack logo">
</p>

<h1 align="center">SheetyStack</h1>

<p align="center"><b>The spreadsheet-native platform — the whole SNCF stack in one CLI.</b><br>
A <a href="https://sncfoundation.github.io">Sheet-Native Computing Foundation</a> distribution · think Rancher/OpenShift, for spreadsheets</p>

---

**Status:** 💾 Autosaving · the platform that bundles the ecosystem.

## What it is

SheetyStack is the **distribution**: one CLI that installs and drives the entire Sheet-Native
stack — [Sheeternetes](https://github.com/sncfoundation/sheeternetes) (orchestration),
[Sheetlium](https://github.com/sncfoundation/sheetlium) (networking),
[Sheetlux CD](https://github.com/sncfoundation/sheetlux-cd) (delivery),
[Sheetstor](https://github.com/sncfoundation/sheetstor) (storage),
[SheetOS](https://github.com/sncfoundation/sheetos), and the whole toolbox
(FinOps, AIOps, WASM, AI, cloud connectors, the forge). It reconciles, together.

## Usage

```bash
sheetystack doctor            # check host deps (git/docker/jq/curl)
sheetystack components        # the catalog + what's installed
sheetystack install all       # git-clone every component + link its CLI
export PATH="$HOME/.sheetystack/bin:$PATH"
sheetystack up                # bring up the shared network (Sheetlium)
sheetystack status            # status of installed components
sheetystack version           # stack + component versions
```

Workspace lives under `SHEETYSTACK_HOME` (default `~/.sheetystack`): components in
`components/`, linked CLIs in `bin/`.

## The stack

| Layer | Component | Analog |
|-------|-----------|--------|
| Orchestration | Sheeternetes | Kubernetes |
| Networking | Sheetlium | Cilium |
| Delivery | Sheetlux CD | Argo CD |
| Storage | Sheetstor | LINSTOR |
| Node OS | SheetOS | Talos |
| Observability | SheetFinOps · SheetAIOps | OpenCost · AIOps |
| Runtime | SheetAssembly | WASM/WASI |
| Intelligence | Sheetelligence | AI copilot |
| Multi-cloud | Cloud connectors | Cluster API |
| Forge | SheetHub | GitLab |

---

<sub>Apache-2.0. Do not run production on a spreadsheet stack. If you do, please film the whole stack.</sub>
