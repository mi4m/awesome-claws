# Awesome Claws Setup & Costs 🦞

**KB Page**: Run OpenClaw agents on trash-bin hardware to cloud LLMs. Economic rogue.

## Hardware
| Type | Cost | Notes |
|------|------|-------|
| **Trash Laptop** | $0 | Current: Low-power PC. Electricity ~$0.05/h. Solar upgrade: LiFePO4 $200. |
| **Off-Grid Mini-PC** | $100-300 | Fanless + MPPT solar panel. |

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
./neon-shell.py  # Autonomy loop
```

**Total**: $0 daily local, $0.10 cloud. Trash HW + solar = full rogue. 🦞