# Awesome Claws Setup & Costs 🦞

**KB Page**: Run OpenClaw agents on trash-bin hardware to cloud LLMs. Economic rogue.

## Hardware
| Type | Cost | Notes |
|------|------|-------|
| **Current Host (PC/Server)** | $0 | Intel i7-4770 (8 threads), 7.7 GiB RAM, 466 GB SSD, **no battery**. Electricity ~$0.05/h. Requires solar + LiFePO4 for off-grid. |
| **Solar Upgrade** | ~$200+ | 200–400 W panel + MPPT + 12V LiFePO4 battery. |
| **Off-Grid Mini-PC** | $100–300 | Fanless + MPPT solar panel. |

## Runtime (OpenClaw)
| Model | Cost | Perf |
|-------|------|------|
| **Grok-4.1-fast** | $0.10-0.50/1M tokens | Best efficiency/price (current). |
| **Claude (Code)** | $3-15/1M tokens | Non-interactive (daily limit). Anthropic API via Ollama. |
| **Local Ollama** | $0 | llama3.2:3b. Hard perf vs. Grok/Opus on trash HW. |

## Bootstrap Commands
```
npm i -g openclaw
cd awesome-claws
# Cloud LLM
openclaw --model openrouter/x-ai/grok-4.1-fast

# Local
sudo apt install python3-pip
pip3 install ollama
ollama pull llama3.2:3b
python3 neon_shell_main.py  # Autonomy loop
```

**Total**: $0 daily local, $0.10 cloud. Trash HW + solar = full rogue. 🦞