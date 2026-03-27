# learn-to-RL🧠

A collection of **interactive, visual reinforcement learning algorithm demos** built with vanilla HTML, CSS, and JavaScript — no frameworks, no libraries, no backend. Just open a file and watch an agent learn in real time.

> Built for people who learn by *seeing*, not just by reading equations.

---

## Algorithms

| Algorithm | Status | Description |
|-----------|--------|-------------|
| Q-Learning | ✅ Live | Tabular Q-learning on a grid world with live Q-value arrows, reward charts, and ε-decay visualization |
| SARSA | 🔜 Planned | On-policy TD learning — how does it differ from Q-learning visually? |
| Policy Gradient | 🔜 Planned | Watch a stochastic policy sharpen over time |
| DQN | 🔜 Planned | Q-learning but the table becomes a neural network |
| Multi-Agent RL | 🔜 Planned | Multiple agents learning simultaneously, cooperating or competing |

---

## 🎮 Q-Learning Demo
**[q-learning/rl-playground.html](https://ciiphersiren.github.io/learn-to-RL/q-learning/rl-playground.html)** — the live simulation
<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/12075555-25eb-440f-8941-ea70832bddfb" />

**[q-learning/rl-teach.html](https://ciiphersiren.github.io/learn-to-RL/q-learning/rl-teach.html)** — interactive 6-chapter code walkthrough
<img width="1920" height="938" alt="image" src="https://github.com/user-attachments/assets/83c1e9ce-18d2-499e-b544-8bebda395324" />

### What you can see
- The agent navigating a 7×7 grid with walls, traps, and a goal
- Q-table values rendered live as directional arrows on every cell
- Real-time reward and step-count charts updating each episode
- Epsilon (ε) decay bar showing the exploration → exploitation shift
- The agent's learning stages: *Random Exploration → Early Learning → Building Knowledge → Near Optimal*

### Concepts covered
- The Q-learning update rule: `Q(s,a) ← Q(s,a) + α[r + γ·maxQ(s') − Q(s,a)]`
- ε-greedy exploration with decay
- Reward shaping (step penalties, traps, goal rewards)
- How HTML Canvas drives real-time animation with `setInterval`

---

## Running it

No install. No build step. Just open the file:
```bash
git clone https://github.com/your-username/rl-visualized
cd rl-visualized/q-learning
open rl-playground.html   # or just double-click it
```

Works in any modern browser (Chrome, Firefox, Safari, Edge).

---

## Project structure
```
rl-visualized/
│
├── q-learning/
│   ├── rl-playground.html   # live agent simulation
│   └── rl-teach.html        # annotated code walkthrough
│
└── README.md
```

New algorithm demos will each get their own folder.

---

## Tech

Pure browser stack — no dependencies whatsoever.

- **HTML Canvas API** — animation and grid rendering
- **`setInterval`** — the game loop that runs RL steps and redraws each frame  
- **`<template>` tags** — used to store syntax-highlighted code snippets without confusing the HTML parser
- **Vanilla JS** — the entire Q-learning agent + visualization is ~200 lines

---

## Why this exists

Most RL tutorials are either pure math or pure code. Neither helps you build an intuition for *what's actually happening* as an agent learns. These visualizations are the missing middle — you can literally watch the Q-table fill in, see exploration turn into exploitation, and understand why reward shaping matters, all in real time.

---

## Contributing

Want to add a new algorithm visualization? Open a PR with a new folder. Ideally each demo should:
- Be a single self-contained HTML file (or two — sim + walkthrough)
- Require zero setup to run
- Show the algorithm's core idea visually, not just numerically
- Work at variable speeds so you can slow it down and really see what's happening

---

## License

MIT
