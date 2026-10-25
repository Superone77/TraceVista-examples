<!-- For maintenance PRs, replace this form with a short description of the change. -->

## Trajectory submission

Submit one representative trajectory per paper for the first round. The complete,
uncompressed `.agent-state.json` must be **5 MB or smaller (5,000,000 bytes)**.

**The TraceVista technical report will cite the source paper of every trajectory
that passes PR review and is included in this library.** Each accepted case will
credit its paper and contributor. Feedback is optional and does not affect acceptance
or citation.

### Paper and contributor

- Paper title:
- Paper link (arXiv, DOI, or publication page):
- Contributor name / GitHub handle:
- BibTeX or full citation:

### Run and export

- Task:
- Agent / framework, model, and relevant configuration:
- Recorded result (success, failure, or not evaluated):
- Export path: `examples/<case-id>.agent-state.json`
- Uncompressed file size in bytes:
- Scope: full run, or excerpt with its event range and necessary context:
- Trajectory source and license / permission to publish:

### What makes this case different?

<!-- Two or three sentences: what does this add to the existing examples?
Consider the task, agent mechanism, exploration, collaboration, recovery, or rollback.
Point to a node or event worth inspecting. Both successful and failed runs are welcome. -->

### Optional feedback

<!-- Leave blank if you prefer. What helped you understand the run? What was
confusing, missing, or incorrect? A sentence or two is enough. -->

- [ ] You may quote my feedback in the technical report and credit me as named above.

### Submission checks

- [ ] The self-contained JSON is at most 5,000,000 bytes and opens in TraceVista.
- [ ] The declared scope retains its original records, call/result links, and necessary source attachments; excerpts and redactions are documented.
- [ ] The paper, task, configuration, and outcome are described in the run overview; annotations match the source records.
- [ ] I added the catalog entry in `examples/index.json`, a thumbnail in `example-thumbnails/`, and the paper, contributor, and source terms in `THIRD_PARTY_NOTICES.md`.
- [ ] I can share this material publicly and have removed credentials and private information.
