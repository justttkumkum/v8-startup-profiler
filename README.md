# Deterministic Crash Reproduction Harness for V8 Experimental Flags

This project provides a tool to help V8 contributors deterministically reproduce crashes caused by experimental flags.
Designed for use during Google Summer of Code 2025.

## 🔧 Features

- Reproduces crash scenarios by running JS under flag combinations
- Logs crash metadata (stderr, stack trace, exit codes)
- Supports delta-minimization of crashing JS (coming soon)
- Verifies if crash is consistent across multiple runs

## 🚀 Getting Started

```bash
git clone https://github.com/justttkumkum/v8-startup-profiler
cd v8-startup-profiler
npm install
bash scripts/setup.sh
```

## 🛠️ Usage

```bash
node harness/runner.js --file testcases/crash1.js --flags="--turbo-collect-feedback-in-generic-lowering"
```

## 📁 Project Layout

- `harness/`: All crash detection + logging logic
- `testcases/`: JS test cases that cause crashes
- `docs/`: Design notes, future plans
- `scripts/`: Setup and automation tools

## 📄 License

MIT

---

GSoC Proposal: [Deterministic Crash Reproduction for V8](https://github.com/justttkumkum/v8-startup-profiler)

Author: Kumkum Kaushik | kumkumkaushik93@gmail.com
