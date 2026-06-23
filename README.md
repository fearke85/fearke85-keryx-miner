# FearMiner

GPU miner for the [Keryx](https://keryx.network/) network — kHeavyHash Proof-of-Work + OPoI AI inference.  
Minerador GPU para a rede [Keryx](https://keryx.network/) — Prova de Trabalho kHeavyHash + inferência de IA OPoI.

---

## Download

Get the latest release at: https://github.com/fearke85/fearke85-keryx-miner/releases/latest

| Platform | File |
|----------|------|
| Windows (self-contained, portable) | `fear-miner-v*-windows.zip` |
| Linux | `fear-miner-v*-linux-amd64.tar.gz` |
| HiveOS | `fear-miner-v*-hiveos.tgz` |

---

## [EN-US] English

FearMiner is a GPU miner for the Keryx network. It combines kHeavyHash PoW with OPoI AI inference on NVIDIA GPUs.

### Quick Start — Windows

1. Download `fear-miner-v*-windows.zip` from the [latest release](https://github.com/fearke85/fearke85-keryx-miner/releases/latest)
2. Extract anywhere
3. Run `allow-in-defender.bat` once (whitelists the unsigned exe in Windows Defender)
4. Run `start-miner.bat` — wizard asks SOLO/POOL, wallet address, and server
5. First run downloads AI models (~a few GB) into `models\` — only once

The zip includes everything: miner, CUDA 12.x runtime, plugins, launchers. No Docker, no CUDA Toolkit required.

### Quick Start — Linux

```bash
tar xzf fear-miner-v*-linux-amd64.tar.gz
cd fear-miner-v*
./keryx-miner -a YOUR_WALLET -s POOL_ADDRESS
```

### Quick Start — HiveOS

```bash
tar xzf fear-miner-v*-hiveos.tgz -C /hive/miners/custom/
miner restart
```

### Requirements

- Windows 10/11 x64 or Linux x64
- **NVIDIA GPU (CUDA)** — required for full mining (PoW + OPoI)
- NVIDIA driver >= 535
- **Inference**: GTX 10xx (Pascal) or newer
- AMD/OpenCL PoW-only available but cannot earn OPoI rewards without NVIDIA GPU

### Important Notes

- **GPU-only inference** — CPU inference (`--cpu-inference`) removed. Per Keryx Labs' upcoming network update, inference is GPU-only.
- **Windows + Defender** — the unsigned exe may trigger a false positive. Run `allow-in-defender.bat` (included).
- **Overclock** — run `apply-overclocks.bat` for per-GPU NVIDIA overclock wizard.
- **Models** — first run downloads the AI models. Copy existing `models\` folder from another rig to skip the download.

---

## [PT-BR] Português

O FearMiner é um minerador GPU para a rede Keryx. Combina PoW kHeavyHash com inferência de IA OPoI em GPUs NVIDIA.

### Início Rápido — Windows

1. Baixe `fear-miner-v*-windows.zip` da [última release](https://github.com/fearke85/fearke85-keryx-miner/releases/latest)
2. Extraia em qualquer pasta
3. Rode `allow-in-defender.bat` uma vez (libera o exe não assinado no Windows Defender)
4. Rode `start-miner.bat` — wizard pergunta SOLO/POOL, carteira e servidor
5. Primeira execução baixa os modelos de IA (~alguns GB) em `models\` — só uma vez

O zip inclui tudo: minerador, runtime CUDA 12.x, plugins, launchers. Sem Docker, sem instalar CUDA Toolkit.

### Início Rápido — Linux

```bash
tar xzf fear-miner-v*-linux-amd64.tar.gz
cd fear-miner-v*
./keryx-miner -a SUA_CARTEIRA -s ENDERECO_POOL
```

### Início Rápido — HiveOS

```bash
tar xzf fear-miner-v*-hiveos.tgz -C /hive/miners/custom/
miner restart
```

### Requisitos

- Windows 10/11 x64 ou Linux x64
- **GPU NVIDIA (CUDA)** — obrigatória para mineração completa (PoW + OPoI)
- Driver NVIDIA >= 535
- **Inferência**: GTX 10xx (Pascal) ou superior
- Mineração apenas PoW via AMD/OpenCL disponível, mas sem recompensas OPoI sem GPU NVIDIA

### Observações Importantes

- **Inferência somente GPU** — inferência via CPU (`--cpu-inference`) removida. A rede Keryx exige inferência exclusivamente em GPU.
- **Windows + Defender** — o exe não assinado pode disparar falso positivo. Rode `allow-in-defender.bat` (incluso).
- **Overclock** — rode `apply-overclocks.bat` para wizard de overclock NVIDIA por GPU.
- **Modelos** — primeira execução baixa os modelos de IA. Copie a pasta `models\` de outro rig para pular o download.

---

## Donate / Doar

FearMiner is free and open-source. If it earns you rewards, consider donating.

| Network | Address |
|---------|---------|
| Keryx | `keryx:qrwhj8cdxgv04pfsjpcqsl9s9urh7nsyyca2ddfhpk96llje6tkc6xhtgu62p` |
| BTC | `1KnUmTATAmfwJPYxi1syfFhCQxJfpGD6XV` (min 0.0001 BTC) |
| USDT (BSC) | `0x52C7118cCF009cd635C684E201B22cFB9F3e8D87` (min 1.00 USDT) |
