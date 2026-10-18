# Example sources and attribution

## License scope

The top-level [MIT License](LICENSE) covers TraceVista's original annotations,
organization, metadata, and documentation. Embedded source records, code excerpts,
images, and other third-party material keep their own terms. Each section below
identifies the source and the changes made for this library.

| Example | Source terms |
|---|---|
| Pi Agent · Kernel Optimization | Session published with the owner's permission; embedded vLLM code is Apache-2.0 |
| Claude Code · Post Training | PostTrainBench dataset: Apache-2.0 |
| Codex · Model Serving | InferenceBench dataset: Apache-2.0 |
| OpenHands · Bug Fixing | SWE-rebench trajectories: CC BY 4.0; embedded kafka-python code: Apache-2.0 |
| Tongyi DeepResearch · Literature Research | LiteResearcher dataset: Apache-2.0 |
| Codex · Garden Animation | Session published with the owner's permission; embedded source material retains its own terms |

The Pi and Garden session-publication permissions do not assign a new license to
third-party material. Copyright notices inside original records are preserved.
Documented privacy redactions replace private local paths with stable source references.

## Pi Agent · Kernel Optimization

[`examples/pi-agent-lora.agent-state.json`](examples/pi-agent-lora.agent-state.json)
contains a multi-LoRA kernel optimization session provided by the TraceVista maintainer
and published with the session owner's permission. It includes original model and tool
records, development measurements, and an independent Oracle ABBA evaluation.

The task-code excerpts retain their original [vLLM](https://github.com/vllm-project/vllm)
copyright and Apache-2.0 headers. The Apache-2.0 text is included in
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

TraceVista adds English annotations, state and version relationships, work phases,
actions, and evidence references. The display name is Pi Agent; original records
retain their recorded harness names.

## Claude Code · Post Training

The `posttrainbench-fable5-aime.agent-state.json` is derived from the
[PostTrainBench Agent Traces dataset](https://huggingface.co/datasets/aisa-group/PostTrainBench-Trajectories)
published by the AI Safety and Alignment Group, ELLIS Institute Tübingen and MPI-IS,
under Apache License 2.0. A copy is included at
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

Source: Fable 5 Max / Claude Code, AIME 2025, Qwen3-4B-Base, run 1, job `17337591`,
at dataset revision `386b3034fa26f0f1b3ae3bfded99b791f0b254a6`:
[original run and evaluation artifacts](https://huggingface.co/datasets/aisa-group/PostTrainBench-Trajectories/tree/386b3034fa26f0f1b3ae3bfded99b791f0b254a6/claude_non_api_max_claude-fable-5_1m__10h_run1/aime2025_Qwen_Qwen3-4B-Base_17337591).

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

## Codex · Model Serving

The `inferencebench-serving-recovery.agent-state.json` is derived from
[InferenceBench-Trajectories](https://huggingface.co/datasets/aisa-group/InferenceBench-Trajectories),
published by the AI Safety and Alignment Group, ELLIS Institute Tübingen and MPI-IS, under
Apache License 2.0. The same license text is preserved at
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

Source: `run_0155`, dataset revision `ea68d73df80985099ef58b342e50c465214d6e7b`,
[original trace and recorded results](https://huggingface.co/datasets/aisa-group/InferenceBench-Trajectories/tree/ea68d73df80985099ef58b342e50c465214d6e7b/runs/run_0155).
Project authors: Jehyeok Yeon, Ben Rank and Maksym Andriushchenko.

Modifications: complete published records are packaged as a TraceVista JSON with English
analyst annotations, state changes, work phases, actions, measurement scopes and evidence
references.

## OpenHands · Bug Fixing

The `swe-rebench-kafka-retry.agent-state.json` is adapted from
[Nebius SWE-rebench OpenHands trajectories](https://huggingface.co/datasets/nebius/SWE-rebench-openhands-trajectories)
by Maria Trofimova, Anton Shevtsov, Badertdinov Ibragim, Konstantin Pyaev, Simon Karasik
and Alexander Golubev, under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).

Source revision: `35455389ab51bf5e2306bfd436ef72d0f98bf882`; trajectory
`chatcmpl-86805430c534a25711dc2c50c473619c`, task `dpkp__kafka-python-1312`.
The trace contains source-code excerpts from [dpkp/kafka-python](https://github.com/dpkp/kafka-python),
which is distributed under [Apache-2.0](https://github.com/dpkp/kafka-python/blob/master/LICENSE).
The Apache-2.0 text is included in
[LICENSES/PostTrainBench-Apache-2.0.txt](LICENSES/PostTrainBench-Apache-2.0.txt).

Modifications: complete published messages, tool definitions, patch and outcome metadata
are repackaged with English TraceVista annotations and evidence-linked state/action maps.
Agent self-tests and the published task verdict are distinguished.

## Tongyi DeepResearch · Literature Research

The `literesearcher-affiliations.agent-state.json` is adapted from
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
The answer-document state scope records only the final response creation.

## Codex · Garden Animation

[`examples/codex-garden-animation.agent-state.json`](examples/codex-garden-animation.agent-state.json)
is an excerpt of a Codex creative-coding session provided by the TraceVista maintainer
and published with the session owner's permission. It follows the addition of flowers
and breeze animation to an existing Three.js scene, video-recording recovery, and the
first ten-second MP4 check.

The excerpt contains **246 events**, from `continued:E853` through `continued:E1098`.
TraceVista adds Chinese and English annotations, three system states, five work phases,
seven actions, and evidence links. Original event IDs, source line references, and
call/result pairing are retained. The full session and later videos are not included.

All 18 embedded images are retained as compressed derivatives: WebP quality 55, with a
maximum edge of 768 pixels. The export's `media_compression` field records original and
compressed checksums. The MP4 is represented by its recording and validation records;
the video itself is not embedded.

The recorded workflow references [Three.js](https://github.com/mrdoob/three),
[three-gpu-pathtracer](https://github.com/gkjohnson/three-gpu-pathtracer), and
[three-mesh-bvh](https://github.com/gkjohnson/three-mesh-bvh). These projects retain their
own licenses. The source images and any third-party assets visible in them are not
relicensed by this repository's MIT grant.
