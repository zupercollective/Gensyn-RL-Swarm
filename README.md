Penulis: [Naufal](https://x.com/0xfal)

> [!NOTE]
> **WHAT IS Gensyn?**\
> Gensyn is a protocol for machine learning computation. It provides a standardised way to execute machine learning tasks over any device in the world. This allows us to aggregate the world's computing supply into a single network, which can support AI systems at far greater scale than is possible today.

# Tutorial Gensyn RL Swarm

## 1. Prerequisites

- [Cara terhubung ke VPS](https://github.com/ZuperHunt/Connect-to-VPS)

## 2. Requirements

### Hardware

| Part | Minimum | Recommended |
| ------------- | ------------- | ------------- |
| CPU | - | ≥ 8 cores |
| RAM | 16 GB | ≥ 20 GB |
| SSD | 50 GB | - |

CUDA devices (officially supported):

| Model | VRAM |
| ------------- | ------------- |
| RTX 4070 | 12 GB |
| RTX 3090 | 24 GB |
| RTX 4090 | 24 GB |
| A100 | 80 GB |
| H100 | 80 GB ~ 94 GB |

### Software

| ✅ Linux | ✅ macOS | ✅ Windows (WSL) |
| ------------- | ------------- | ------------- |

> [!NOTE]
> Tutorial ini dibuat menggunakan Linux (Ubuntu), untuk sistem operasi lainnya mungkin akan sedikit berbeda!

## 3. Dependencies

### 3.1 System Packages

```
sudo apt update && sudo apt upgrade -y
```

### 3.2 Install Other Essential Packages

```
sudo apt install -y screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev
```

### 3.3 Install Python

```
sudo apt install -y python3 python3-pip python3-venv python3-dev
```

### 3.4 Install Node.js and Yarn

```
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash - && sudo apt install -y nodejs && sudo npm install -g yarn
```

## 4. Execution

### 3.1 Create a Session

Ubah `<SESSION_NAME>` menjadi terserahmu.

```
screen -S <SESSION_NAME>
```

### 4.2 Clone the Repository

```
git clone https://github.com/gensyn-ai/rl-swarm/
cd rl-swarm
```

### 4.3 Import swarm.pem (Optional)



### 4.4 Run the swarm

```
python3 -m venv .venv
source .venv/bin/activate
sed -i '/[ -z "$PS1" ] && return/i : "${PS1:=}"' /root/.bashrc
./run_rl_swarm.sh
```

Pilih `a` untuk CPU-only atau GPU dengan VRAM kecil, pilih `b` untuk GPU dengan VRAM besar.

![image](https://github.com/user-attachments/assets/3efc2da2-6a07-4587-8887-32d1f3886f1f)

Pilih saja `n`.

![image](https://github.com/user-attachments/assets/ad674908-d208-4b9c-b7fc-1df68e30f9b4)

---

Reach us if you have any question:\
ZuperCollective's [Discord server](https://discord.gg/ZuperCollective) | [X(Twitter)](https://twitter.com/ZuperCollective)

# Acknowledgements

* [RL Swarm](https://github.com/gensyn-ai/rl-swarm)
