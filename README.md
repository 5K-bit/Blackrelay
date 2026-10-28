<div align="center">

<img src="assets/brand/github-banner.svg" alt="BlackRelay — Bounded local workflow dispatch. A Blackfong project." width="1200">

**Bounded local workflow dispatch.**

![Stage](https://img.shields.io/badge/stage-MVP%20scaffold-7ca8ff?style=for-the-badge&labelColor=0c1220)
[![CI](https://img.shields.io/github/actions/workflow/status/5K-bit/Blackrelay/obeos-component-ci.yml?branch=main&style=for-the-badge&label=CI&labelColor=0c1220&color=7ca8ff)](https://github.com/5K-bit/Blackrelay/actions/workflows/obeos-component-ci.yml)

[Architecture](docs/blackrelay-concept1.md) · [Integration contract](docs/obeos-integration-contract.md)

</div>

---

# BlackRelay

| Trigger | Route | Stage |
|---|---|---|
| Local file and event activity | Bounded adapters and explicit actions | Architecture and MVP scaffold |

BlackRelay is a local-first workflow dispatcher for the Blackfong/OBEOS ecosystem. It reacts to local file or event activity and routes actions through bounded adapters.

Current status: planned / MVP scaffold.

BlackBus moves events. BlackRelay reacts to events.

Canonical ownership: this repository is the source of truth. OBEOS consumes BlackRelay as a pinned component/submodule rather than maintaining a second editable copy.

See `docs/blackrelay-concept1.md` for the current architecture and MVP definition.
