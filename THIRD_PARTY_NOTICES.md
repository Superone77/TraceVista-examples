# Example sources and attribution


The bundled Pi Agent multi-LoRA JSON export is a user-authorized public research example,
with English annotations and original model/tool evidence. It includes task-code excerpts
with their original vLLM copyright and Apache-2.0 headers. The upstream viewer license
does not cover the research logs. Other imports are not bundled. The presentation is named
Pi Agent; historical harness names inside original evidence remain unchanged.

### PostTrainBench

The bundled `posttrainbench-fable5-aime.agent-state.json` is derived from the
[PostTrainBench Agent Traces dataset](https://huggingface.co/datasets/aisa-group/PostTrainBench-Trajectories)
published by the AI Safety and Alignment Group, ELLIS Institute Tübingen and MPI-IS,
under Apache License 2.0. A copy is included at
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

Source: Fable 5 Max / Claude Code, AIME 2025, Qwen3-4B-Base, run 1, job `17337591`,
at dataset revision `386b3034fa26f0f1b3ae3bfded99b791f0b254a6`:
[original run and evaluation artifacts](https://huggingface.co/datasets/aisa-group/PostTrainBench-Trajectories/tree/386b3034fa26f0f1b3ae3bfded99b791f0b254a6/claude_non_api_max_claude-fable-5_1m__10h_run1/aime2025_Qwen_Qwen3-4B-Base_17337591).
Selected for this library on 2026-10-04.

Modifications: the source trace and evaluation artifacts are repackaged as one TraceVista
JSON export, with English analyst annotations, state/checkpoint relationships, work phases,
actions and evidence references. Original messages, commands, results and attached evidence
retain their source text. The 30% archived final score, 23.3% pooled development score and
current v1.2 aggregate are recorded separately.

The added selection manifest replaces local collection paths with
`source://posttrainbench/` references. Filenames, public source URLs, and the original
experiment records are preserved. Original and redacted manifest checksums are recorded
separately.

Project: [PostTrainBench](https://posttrainbench.com/), by Ben Rank, Hardik Bhatnagar,
Ameya Prabhu, Shira Eisenberg, Karina Nguyen, Matthias Bethge and Maksym Andriushchenko.
Paper: [PostTrainBench: Can LLM Agents Automate LLM Post-Training?](https://arxiv.org/abs/2603.08640), ICML 2026.

### InferenceBench

The bundled `inferencebench-serving-recovery.agent-state.json` is derived from
[InferenceBench-Trajectories](https://huggingface.co/datasets/aisa-group/InferenceBench-Trajectories),
published by the AI Safety and Alignment Group, ELLIS Institute Tübingen and MPI-IS, under
Apache License 2.0. The same license text is preserved at
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

Source: `run_0155`, dataset revision `ea68d73df80985099ef58b342e50c465214d6e7b`,
[original trace and recorded results](https://huggingface.co/datasets/aisa-group/InferenceBench-Trajectories/tree/ea68d73df80985099ef58b342e50c465214d6e7b/runs/run_0155).
Project authors: Jehyeok Yeon, Ben Rank and Maksym Andriushchenko.

Modifications: complete published records are packaged as a TraceVista JSON with English
analyst annotations, state changes, work phases, actions, measurement scopes and evidence
references. No benchmark was rerun. Selected on 2026-10-04.

### SWE-rebench OpenHands trajectories

The bundled `swe-rebench-kafka-retry.agent-state.json` is adapted from
[Nebius SWE-rebench OpenHands trajectories](https://huggingface.co/datasets/nebius/SWE-rebench-openhands-trajectories)
by Maria Trofimova, Anton Shevtsov, Badertdinov Ibragim, Konstantin Pyaev, Simon Karasik
and Alexander Golubev, under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).

Source revision: `35455389ab51bf5e2306bfd436ef72d0f98bf882`; trajectory
`chatcmpl-86805430c534a25711dc2c50c473619c`, task `dpkp__kafka-python-1312`.
The trace contains source-code excerpts from [dpkp/kafka-python](https://github.com/dpkp/kafka-python).

Modifications: complete published messages, tool definitions, patch and outcome metadata
are repackaged with English TraceVista annotations and evidence-linked state/action maps.
Agent self-tests and the published task verdict are distinguished. This visualization was
created on 2026-10-04; it does not imply endorsement by the dataset or software authors.

### LiteResearcher SFT trajectories

The bundled `literesearcher-affiliations.agent-state.json` is adapted from
[LiteResearcher-SFT-Data](https://huggingface.co/datasets/simplex-ai-inc/LiteResearcher-SFT-Data),
published by simplex-ai-inc under Apache License 2.0. The same license text is preserved at
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

Source revision: `5c8caa17121e216f8ad8f928e6a8d4f51d3fefee`, configuration `default`,
split `train`, zero-based row `60000`, question pool `MiroRL_GenQA`.
[Pinned dataset card](https://huggingface.co/datasets/simplex-ai-inc/LiteResearcher-SFT-Data/blob/5c8caa17121e216f8ad8f928e6a8d4f51d3fefee/README.md)
and [source row](https://huggingface.co/datasets/simplex-ai-inc/LiteResearcher-SFT-Data/viewer/default/train?row=60000).
Paper: [LiteResearcher: A Scalable Agentic RL Training Framework for Deep Research Agent](https://arxiv.org/html/2604.17931v1),
by Wanli Li, Bince Qu, Bo Pan, Jianyu Zhang, Zheng Liu, Pan Zhang, Wei Chen and Bo Zhang.

The paper attributes the SFT trajectories to a Tongyi DeepResearch teacher using online
tools. This row is a released teacher conversation, not a LiteResearcher-4B execution.
Its task is to compare the affiliations of Claudia Hohmann and Felix Tettenborn in two
December 2020 journal articles. The published final answer names Fraunhofer ISI.

Modifications: all 15 source messages are retained in one self-contained TraceVista export,
with English state, work-stage and action annotations. The XML thinking, tool-call,
tool-response and answer spans are separated into 22 events without changing their text.
Tool observations originally encoded as user turns are displayed as results. Call identifiers
are explicitly marked as adapter-created pairs; native IDs, exact model checkpoint,
hardware, budgets, timing and independent answer grading are not supplied by the row.
The answer-document state scope records only the final response creation. Selected on
2026-10-05; no underlying research episode was rerun.
