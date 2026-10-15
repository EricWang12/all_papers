# Reader profile

Everything the paper-explain skill personalizes is in this file. It lives in the
library repo, so every machine and every agent reads the same profile. Edit it freely.
The skill also edits it, then commits and pushes, when your feedback is about how you like
papers explained in general rather than about one paper.

## How I learn

- **Language.** Write pages in Chinese by default, and keep the key concepts in English:
  method and module names and terms of art (verifier, retargeting, self-evolving tool
  library). Section names stay English (Problem, Big picture, Stages).
- **Visual first.** Anything with a flow becomes a flowchart. A picture beats a paragraph.
- **Problem first, told on the example.** Open with the problem, explained on the running
  example rather than as a literature survey:
  - what the example's input is and what we want out of it;
  - which baselines the paper builds on or compares against;
  - for each baseline, what it does and the exact step where it breaks on this
    example, with its number;
  - then one line on the root cause.
  Keep it short: one flowchart and a table of at most 4 rows.
- **Order.** Problem, then Big picture right after it, then Stages, then Details. The
  running example is introduced inside the problem, not as its own block in between.
- **Concise, TL;DR style, but complete.** Bullets and short phrases, no paragraphs.
  Coverage comes from the hierarchy, not from longer text.
- **Hierarchical.** Level 1 is the big idea, Level 2 is the stages as a flowchart, and
  Level 3 goes into each stage in more detail.
- **One running example.** Follow one concrete example from input to output through
  every stage. It should be rich enough to touch every idea in the paper, with its
  values shown inside the flowcharts.
- **The authors' figures.** Inspect the original figures and explain with them, pointing
  at their parts. The authors' figure is the most precise description; my flowcharts
  complement it.

## My projects

Each project is one folder in the library. The scope line decides where a paper goes.
"Our work" helps write the page's "What to take from it" section.

| Folder | Project | What belongs here | Our work |
|---|---|---|---|
| `Robotic-harness` | Robotic harness | Harnesses that let LLM/VLM agents drive robots: agent runtimes and supervisors, coding agents as robot policies, tool and skill libraries, code-as-policy, agentic planning and verification, benchmarks for agent-controlled manipulation. | `robot-harness-robodojo-mas/robot-harness`: one Runtime running Native API, Codex and Claude Code policies on RoboTwin, LIBERO/LIBERO-Pro and RoboDojo; a Supervisor owns robot mutation, admission and evidence. Real arms: SO-101 (`Real-Robotics/`). |
| `Agent-centric-real-to-sim` | Agent-centric real-to-sim | Agents that turn the real world (videos, scans, photos, prompts) into simulation: scene and room reconstruction, asset and articulation generation, human and object motion into sim, digital twins, world building and world models for training or evaluating robots. | `Harness-WM/real2sim-anything-indoor` (video → Blender room, GVHMR human motion), WorldClaw skills (prompt → white-box scene → Genesis sim → render), notes in `Harness-WM/world-building-landscape.md`. |

## Library

- Repo: https://github.com/EricWang12/all_papers.git. This folder is its clone. Every
  run pulls first, then commits and pushes its results. Commits here are always
  authorized.
- Lab-machine clone: `/nfs/turbo/coe-jungaocv/wzn/workspace/papers`
- Artifact title: Zhaoning Paper Pile
- Artifact: https://claude.ai/artifact/GGxYmvE3MgSAJUQDSi9EHb (first published 2026-10-15)

## Feedback log

- 2026-10-15: initial profile, written from the first conversation.
- 2026-10-15, after DexAgent v1:
  - Pages are in Chinese, with the key concepts in English.
  - Big picture comes directly after the problem.
  - The problem section was too verbose and never showed where things break, or what the
    baselines' problems are. Tell it on the running example, one baseline at a time.
- 2026-10-15: library synced to GitHub (all_papers); the artifact is named "Zhaoning Paper Pile"; this profile moved into the library repo.
- 2026-10-15: PDFs stay out of git (`.gitignore`), because git history never shrinks. Each page records a versioned PDF link (`paper:pdf`) for re-downloading.
