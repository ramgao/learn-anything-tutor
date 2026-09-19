# Learn Anything Tutor

An open Codex skill for teaching almost any subject through adaptive explanations, learner practice, and useful feedback. It includes practical routes for technology and cybersecurity learning.

**Goal:** help someone perform independently. The skill does not promise a perfect AI teacher. It makes the tutor look for evidence of understanding and adjust its next move.

## What makes it useful

- Starts with the learner's real goal and a small diagnostic, instead of a generic lecture.
- Switches between concise answers and deeper tutoring according to the request.
- Uses worked examples, active practice, specific feedback, and later retrieval when they fit.
- Gives hints in proportion to productive struggle, then fades help as skill grows.
- Checks independent application and transfer before calling something learned.
- Teaches technology through observable examples, predictions, and explanations of mechanisms.
- Grounds cybersecurity exercises in local labs, intentionally vulnerable practice targets, and authorized systems.
- Verifies current or high-stakes facts and turns sources into usable decisions.
- Treats the original teaching patterns as hypotheses open to testing, not proven breakthroughs.

## Install in Codex

Clone this repository into your Codex skills directory, usually `~/.codex/skills/learn-anything-tutor`. Restart Codex or refresh skills if needed. The entrypoint is [`SKILL.md`](SKILL.md); Codex can select it for tutoring requests or you can invoke `$learn-anything-tutor` explicitly.

On Windows PowerShell:

```powershell
git clone https://github.com/ramgao/learn-anything-tutor.git "$env:USERPROFILE/.codex/skills/learn-anything-tutor"
```

## Try it

```text
Use $learn-anything-tutor to teach me probability from zero. I have 20 minutes. Ask me one question at a time.
```

```text
Use $learn-anything-tutor to teach me HTTP from zero so I can read bug bounty reports. Use a local practice example and check my understanding.
```

```text
Use $learn-anything-tutor to help me debug my SQL query. Give hints before revealing the corrected query.
```

## How the tutor works

```text
Goal → smallest diagnostic → short model → learner attempt → precise feedback
                                              ↘ adapt support ↗
              → independent task → new-context task → later retrieval
```

The tutor can skip or compress steps when the learner asks for a quick answer. The full operating instructions are in [`SKILL.md`](SKILL.md). The five proposed design patterns are explained in [`references/design-patterns.md`](references/design-patterns.md), example conversations in [`references/examples.md`](references/examples.md), and the research basis and limits in [`references/evidence.md`](references/evidence.md).

## Why the research matters

The design draws on research on practice testing and spacing, worked examples, active learning, feedback, metacognition, and the risks of unguided AI help. See the [source table](references/evidence.md). Evidence for those components is not evidence that this exact skill has been validated. To evaluate it, compare independent and delayed performance across subjects and learners, and report failures as well as successes.

## Contribute

Open an issue with a realistic learner request, the tutor's response, the observed difficulty, and a proposed improvement. Avoid including private learner data. Contributions that claim better learning outcomes should include a comparison and an assessment the learner completed without help.

## License

MIT; see [LICENSE](LICENSE).
