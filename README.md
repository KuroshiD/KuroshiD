<div align="center">

<img src="https://capsule-render.vercel.app/api?gtype=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Kuroshi&fontSize=60&fontColor=ffffff&fontAlignY=38&animation=fadeIn" alt="Kuroshi banner" width="100%"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=BD93F9&center=true&vCenter=true&width=620&lines=Full-Stack+Development;AI+Research;Search+%26+Planning;Reinforcement+Learning)](https://github.com/KuroshiD)

[![Profile views](https://hits.sh/github.com/KuroshiD/KuroshiD.svg?style=flat-square&label=profile%20views&color=8A2BE2)](https://hits.sh/github.com/KuroshiD/KuroshiD/)

</div>

---

## About

<img align="right" width="260" src="https://raw.githubusercontent.com/KuroshiD/KuroshiD/main/e18518c6d24257c6fb02e3c95a862d85.gif" alt="GIF"/>

Full stack developer aiming for a career in AI research.

My interests are reinforcement learning, supervised learning, classical AI (search and planning) and symbolic AI. I also enjoy the functional paradigm.

Catholic.

<br clear="right"/>

## Stack

**Day to day**

<img src="https://skillicons.dev/icons?i=cpp,go,py,ts,js&theme=dark" alt="Tech stack"/>

**Learning**

<img src="https://skillicons.dev/icons?i=py,rust&theme=dark" alt="Learning"/>

## Featured project

### KAIROS

A chess agent that separates *how good* a move is from *how much it looks like* a given style. It is an academic computer science project (Integrative Project, Artificial Intelligence and Data Science, 2026) that asks whether an AI can learn different styles of chess and reproduce them without needlessly giving up objective move quality.

Three components work together:

- **Stockfish** analyzes each position (MultiPV) to build a tree of candidate moves with objective evaluations in centipawns, cached in SQLite.
- **A residual CNN** (18×8×8 input, ten residual blocks with Squeeze-and-Excitation, 1,968-logit policy head) learns move preferences. It is trained on human games and Lichess puzzles, then fine-tuned per style on games from 20 players grouped a priori: 11 romantic (e.g. Morphy, Anderssen, Tal, Kasparov) and 9 positional, used as a control (e.g. Karpov, Petrosian, Capablanca).
- **Alpha-beta minimax** searches that tree. The agent's moves maximize U = v(leaf) + λ · Σ log π(a | s), where v is the Stockfish value and π is the style policy. The opponent minimizes and has no style. λ is measured in centipawns per nat.

With λ = 0 the agent plays the objective decision of the same search. Positive values let the learned style influence the choice, at a cost measured in centipawns.

What the experiments show so far:

- Divergence from the objective move grows with λ. At depth 1 with the romantic policy it goes from 0.176 at λ = 5 to 0.476 at λ = 160, with an average cost of 1.0 to 12.1 cp.
- On held-out games, the romantic policy explains romantic players' moves better than the positional control (NLL difference of −0.032, 95% CI excluding zero).
- That difference does not reach the chosen moves. The romantic, positional and untuned policies pick almost the same moves (divergence of 0.328 against 0.337 at λ = 20), so behavioral differences between styles are **not confirmed at the agent level**. The stylistic signal lives in the probability distribution, not in the argmax.

These results come from a single seed and are exploratory. KAIROS is not meant to beat Stockfish. It studies how machine learning and heuristic search can be integrated, and how stylistic preference trades off against objective quality. It also ships with a local web interface to play against the agent and tune λ.

<img src="https://skillicons.dev/icons?i=py,pytorch&theme=dark" alt="Project stack"/>

[Repository](https://github.com/KuroshiD/KAIROS)

## Away from the keyboard

Light novels, manga, manhwa, chess and gym.

Favorite novel: **Lord of the Mysteries**.

## GitHub stats

<div align="center">
<br/>

<img src="https://streak-stats.demolab.com?user=KuroshiD&theme=transparent&hide_border=true&ring=bd93f9&fire=bd93f9&currStreakLabel=bd93f9&sideLabels=8b949e&currStreakNum=8b949e&sideNums=8b949e&dates=8b949e" alt="Streak"/>

</div>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" width="100%" alt="footer"/>
</div>
