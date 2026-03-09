# Edictum

**Runtime governance for AI agent tool calls.**

Edictum enforces deterministic YAML contracts on every tool call your agents make — outside the LLM, at the infrastructure layer. Governs what agents *do*, not what they *say*.

### Repositories

| Repo | Description | License |
|---|---|---|
| [edictum](https://github.com/edictum-ai/edictum) | Core governance library (`pip install edictum`) | MIT |
| [edictum-console](https://github.com/edictum-ai/edictum-console) | Self-hostable operations console — approvals, fleet monitoring, contract management | [FSL-1.0-Apache-2.0](https://fsl.software) |

### Quick Start

```bash
pip install edictum
```

```python
from edictum import Edictum, EdictumDenied

guard = Edictum.from_yaml("contracts.yaml")
result = await guard.run("read_file", {"path": ".env"}, read_file)
```

### Links

- 📖 [Documentation](https://docs.edictum.ai)
- 🌐 [Website](https://edictum.ai)
- 📦 [PyPI](https://pypi.org/project/edictum/)
- 📄 [GAP Paper](https://arxiv.org/abs/2602.16943) — *Mind the GAP: Text Safety Does Not Transfer to Tool-Call Safety*
