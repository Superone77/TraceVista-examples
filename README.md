# TraceVista examples

Public example trajectories for [TraceVista](https://github.com/Superone77/TraceVista), kept separately from the viewer and conversion skill. Each case is one self-contained `.agent-state.json`, with analyst annotations linked to preserved source records. Browse them on the [TraceVista website](https://tracevista.pages.dev/).

## Cases

| Case | Scope |
|---|---|
| [Pi Agent · Kernel Optimization](https://tracevista.pages.dev/?example=pi-agent-lora) | Multi-LoRA kernel optimization, direct launches, an identity-cache regression, and independent Oracle ABBA evaluation. |
| [Claude Code · Post Training](https://tracevista.pages.dev/?example=posttrainbench-fable5-aime) | AIME 2025 post-training of Qwen3-4B, fine-tuning, checkpoint averaging, and final model selection. |
| [Codex · Model Serving](https://tracevista.pages.dev/?example=inferencebench-serving-recovery) | Mistral-7B serving, scheduler trials, startup recovery, and a reverted sampling experiment. |
| [OpenHands · Bug Fixing](https://tracevista.pages.dev/?example=swe-rebench-kafka-retry) | Kafka retry repair, local self-tests, and the published task outcome. |
| [Tongyi DeepResearch · Literature Research](https://tracevista.pages.dev/?example=literesearcher-affiliations) | A released LiteResearcher teacher conversation comparing authors' affiliations in two journal articles. |
| [Codex · Garden Animation](https://tracevista.pages.dev/?example=codex-garden-animation) | A fixed excerpt covering Three.js flowers, breeze animation, video-recording recovery, and a ten-second MP4 check. |

`examples/index.json` lists the cases in website order, with Pi Agent first. Complete exports live in `examples/`; thumbnails live in `example-thumbnails/`. Source attribution and terms are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md), with license copies in `LICENSES/`. TraceVista's MIT code license does not replace these source terms.

## Use with the viewer

Place this repository beside the viewer checkout:

```text
parent/
├── TraceVista/
└── TraceVista-examples/
```

From the viewer repository, clone this library and use the data revision recorded in `examples.lock.json`. Skip the clone command if you already have the sibling checkout:

```bash
git clone --no-checkout https://github.com/Superone77/TraceVista-examples.git ../TraceVista-examples
example_revision="$(node -p "require('./examples.lock.json').revision")"
git -C ../TraceVista-examples fetch origin "$example_revision"
git -C ../TraceVista-examples checkout --detach "$example_revision"
pnpm test:examples
pnpm dev:site
```

Open [localhost:8876](http://127.0.0.1:8876/). `pnpm build:site` writes the showcase to `dist-site/`. For another location, prefix the viewer command with `TRACEVISTA_EXAMPLES_DIR=/path/to/TraceVista-examples`. This repository root contains `examples/index.json`; do not point the variable at `examples/` itself.

The viewer's default `pnpm dev`, `pnpm test`, and `pnpm build` work without this library. You can also import any individual complete export into the [hosted viewer](https://tracevista.pages.dev/).

## Preserve and update a case

Preserve original event text, event IDs, call/result pairing, and source attachments. Before publishing, replace private local paths with stable source references, including paths inside embedded source text. Record redactions and their checksums. Summaries and inferred relationships must cite evidence. Recorded results, local self-tests, independent evaluation, and benchmark verdicts keep their own scope; converting or validating an export does not rerun the underlying experiment.

The Garden Animation export covers only events `continued:E853` through `continued:E1098` of a longer session. Keep that exact self-contained excerpt and its thumbnail. The full session export and later videos are excluded.

For an approved data update:

1. Update the complete export, catalog, thumbnail, and source notices as needed.
2. Commit the data changes in this repository.
3. From the viewer checkout, run `pnpm examples:lock -- ../TraceVista-examples` to record the new data commit and SHA-256 of the served files.
4. Run `pnpm test:examples` and `pnpm build:site`, inspect the showcase, and commit the viewer's updated `examples.lock.json`.

The generated `tracevista-release.json` records the viewer revision and dirty state, plus the example revision and lock-file hash. Keep it with each deployed showcase so a release can be traced to both repositories.

## Main branch protection

Changes to `main` require a pull request and one approving review. New commits dismiss
stale approvals; the rules also apply to administrators. Force pushes and branch deletion
are disabled. The settings are recorded in [.github/main-protection.json](.github/main-protection.json),
and [.github/CODEOWNERS](.github/CODEOWNERS) names the maintainer.
