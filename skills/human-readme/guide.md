[English](guide.md) · [中文](guide_cn.md) · [← the human-readme workflow](../../README.md)

# 📖 Docs for human readers

Documentation rules you follow as the project develops, so that a first-time visitor quickly
understands what the project is for, gets a first result along the shortest default path, and
knows where to go next. They work with or without agents. The human-readme workflow
([`SKILL.md`](SKILL.md)) follows them step by step; the checklist below is the short version.

> **Why:** an AI reads everything at once, so agent-written READMEs tend to pile every feature
> side by side. People usually scan headings and pick one path; a flat pile is hard to take in,
> and an unclear purpose makes the whole page harder to follow.

## ✔️ Checklist

- Before writing: decide the reader, their task and what "done" looks like; if unsure, write for a first-time user. Find the page that already covers it.
- Under the title, one line of contents: links to every `##` section, separated by ` · `; an outside entry point (e.g. a catalog of things to install) goes last, in bold.
- Highlight: the first sentence says who it is for and what problem it solves, plus one visible result; when readers will compare it with something they know, the difference right after (a table on the same points if there are several), fair to the other.
- Install and first run: one default path; prerequisites before the step that needs them; one line per kind of computer, saying which line easily confused cases take; numbered steps, one action each, starting with how to open the terminal; a prompt met in a step gets one line there and a link to a list at the end. When there are several ways to install, say they are alternatives (a "pick one" table, Option A / Option B), not steps in a row.
- For installed tools, separate sections in this order: system requirements, install, every day, then an example whose first sentence says what it shows and makes; where the user's files live goes on its own page.
- What you can do: a few common reader tasks, one line and one link each. Common problems: only real, recurring ones.
- Keep out of the README: full option tables, detailed internal architecture, history, ledgers, agent instructions, unshipped features. Each fact has one source of truth.
- Sub-pages serve one purpose each (tutorial, how-to, reference, explanation). A metric the project defines itself gets one reference page.
- Each `##` heading starts with an emoji; content comparing items on the same points goes in a table; a table cell with more than one short sentence becomes points (`• a<br>• b`).
- Before delivering: walk the default path and report where it was verified, the result and what was not verified; local links and anchors resolve.

## 🧭 Three principles

1. **Funnel:** go from "what and why" to the details, so a reader gains something wherever they
   stop. The README carries only the most common path; details are a link away.
2. **Each fact has one source of truth:** each command, option or version requirement is
   maintained on one page. A minimal command on the README, a summary, or the other-language
   version may repeat it, but update them together; prerequisites a step needs are stated right
   before that step, not only behind a link.
3. **Judge by the reader's task:** good docs let the reader understand, run and find the next
   step. Length and a full set of headings are not the measure.

## 🏠 The README in four parts

This is the default skeleton, not a fixed layout for every project: for a dataset or a rules
library, "install" becomes "the shortest way to get and use it"; for a mature README, change it
only where the reader's task calls for it, not to fit the template.

| Order | Part | Must | Avoid |
| --- | --- | --- | --- |
| 1 | **Highlight** | • First sentence: who it is for and what problem it solves<br>• If readers will compare it with something they already know (for example a feature their platform has built in), right after it one sentence on the difference, and a table comparing the two on the same points when there are several; say fairly what the other can do<br>• Then a few evidenced differences and one visible result (screenshot, command output, input/output pair) | Listing every feature; adjectives nobody can check; leaving the obvious "how is this different from X?" open, or running X down |
| 2 | **Install and first run** | One default path end to end; when there are several ways to install, say first that they are alternatives (a "pick one" table, then Option A / Option B), so they do not read as steps in a row; prerequisites (OS, account, GPU, cost) right before the step that needs them; say where the input comes from; end with a minimal example and what success looks like<br>• Readers on different computers: one line per kind of computer, and say which line the easily confused cases take (e.g. WSL on Windows still uses the Windows installer)<br>• For something people install: a system-requirements section right before install, one row per kind of computer (OS version; runtime versions such as Python 3.9 or newer; what the installer installs itself; how to check, and upgrade, what it does not); then separate sections in this order: install (only installing), every day (how to start), then an example, titled as one, whose first sentence says what it shows and what it makes (e.g. "write down one way you do your work: it becomes a workflow you can run"), and that refers to the daily steps instead of repeating them<br>• Where the user's files live and how to find them from their usual file manager (e.g. the WSL home, not the Windows disk): its own page, linked from a row of the "what you can do" table, not a README section<br>• Steps numbered, one action each; the first step says how to open the terminal the commands go into (e.g. Windows: open PowerShell, type `wsl`); a step the reader does not strictly need (e.g. a practice folder) says why it is there<br>• A prompt the reader meets in a step (e.g. `Where should Durweg be installed?`): one line at that step on what to choose, linking to a list at the end of the README, one item per line, each with a link to its page | Every platform's full branch on the front page; stopping at "installed"; several actions in one paragraph |
| 3 | **What you can do** | Reader tasks ("restore your setup on another machine"), one line and one link each; module names may be added as a hint; only the common ones, the full catalogue on its own page | Module names alone; option details |
| 4 | **Common problems** | Only real, recurring problems that the main path cannot remove; one line plus a troubleshooting link each | Invented questions to fill the section; FAQ entries that paper over broken install steps |

Close with one line: more docs · help · license. **Skip a part that has no content yet** rather
than leaving an empty heading.

**Keep out of the README:** full option tables, detailed internal architecture (a one- or
two-sentence overview is fine), development history, experiment ledgers, agent instructions,
unshipped features.

## 📂 Sub-pages: one purpose each

Each page the README links to serves one purpose (from [Diátaxis](https://diataxis.fr/)):

| Purpose | The reader thinks | Example |
| --- | --- | --- |
| Tutorial | "Walk me through it" | First complete example from scratch |
| How-to guide | "I need to get this done" | Move to a new machine, add a GPU server |
| Reference | "What does this option do?" | Config keys, command-line flags |
| Explanation | "Why is it built this way?" | Architecture, trade-offs, limits |

You do not need four directories on day one. A small project needs a README and a few how-to
pages; split further as it grows. Mixing is the usual failure: when a how-to grows a long
explanation, move it to its own page and leave a link.

### Project-specific metrics and formulas

A metric or formula the project defines itself (not common knowledge such as MAE or accuracy)
gets one page, e.g. `docs/metrics.md`. It is reference and explanation, so it is a sub-page;
the README's "What you can do" keeps one line linking to it. Readers, including the author a
month later, forget what a home-made number means.

- **Open with a lookup table**: "I want to know … → look at metric …", each row linking to its
  section.
- **Notation and regions first**: define every symbol once. When metrics refer to regions,
  masks or other spatial notation, add one diagram of them.
- **Per metric**, in this order:
  - **Question**: what it answers, in one sentence.
  - **Formula**: written exactly as the code computes it.
  - **How to read the value**: what 0, 1, above 1 and negative values mean, and when it
    cannot be computed (e.g. an empty region, a zero denominator).
  - **Criterion**: the threshold that counts as success, if there is one.
  - **Actual results**: typical values with their source (run name, table).
  - **Implementation**: function and file, linked.


## 📋 Headings and tables

Each `##` section heading of a README starts with one emoji that hints at the section (for example
💻 System requirements, 🧭 Install, 📅 Every day, 🚀 Example, 🙋 I want to …, 🛠️ Common problems),
so a reader scanning the page finds the section by eye. Content that compares items along the same
points (one row per computer, per file, per task, per question) is written as a table; steps that
are done in order stay a numbered list. In-page links then point at the anchor with a leading
hyphen (`#-example-write-down-your-method`).

### A line of contents under the title

Right under the title, one line links to every `##` section of the README, in order, separated
by ` · ` and using the same emoji as the headings, so a reader sees the whole page at a glance
and jumps to the part they need. An entry point outside the README that many readers look for
(e.g. a catalog of workflows to install) goes last, in bold. Only `##` sections: the line stays
one line. Example: the [Durweg README](https://github.com/musetee/durweg#durweg).

### Explanations in tables

A table cell that explains something in more than one short sentence is split into points, one
per line, so the table stays narrow enough to read. GitHub tables cannot hold Markdown lists, so
write `• point<br>• point`. Keep the content: split it, do not cut it. A cell of one short clause
stays as it is. Example: the tables in the [Durweg README](https://github.com/musetee/durweg#durweg).

## 🔄 As the project develops

| When | Do |
| --- | --- |
| **Before writing** | Decide who this is for, what they want to do, and what "done" looks like; look for the page that already covers it. If unsure, write for someone using the project for the first time. |
| **New project** | Write the highlight and "install and first run", plus one line pointing to further reading. |
| **New feature** | Ask: can readers now do something new? Add a README line only if new users need to find it; put steps in a how-to and options in the reference. Not every feature needs a page. |
| **Bug fix** | Fix the original steps first. Only a recurring problem the main path cannot remove goes to troubleshooting or the FAQ. |
| **Release or removal** | Check examples against the current version; remove links to removed features; link migration notes for breaking changes. |

## ✅ Before delivering

1. Walk the default path from prerequisites to the success result; write down where it was
   verified, what came out, and what was not verified. "The command looks right" is not
   verification.
2. Local links and anchors resolve.
3. Answer four questions: from the first screen, can a reader say what the project is for? Pick
   the default path? Recognise success? Find the next step?

| Check | How |
| --- | --- |
| Local links, anchors, Markdown; the required content (purpose, default starting path) is there | Automatic; fix on failure |
| The default example runs | Run it automatically when you can; when it needs an account, hardware or payment, state what was verified |
| Growing length, long paragraphs, deep headings, external links temporarily down | Warning only; a person decides |
| Readers understand and get it running | When the getting-started path is first written or substantially changed, and someone is available, have a person who did not build it try the task; an agent simulation only supplements this. Smaller edits need only the self-check above |

There is no hard length limit: word or code-block caps reward squeezing several steps into one
block, which is harder to follow. Do not promise a duration in general either; if you state
one, measure it under the stated prerequisites.

## ✏️ Changing these rules

These rules change with use. When a rule does not fit a real README, or you have a new
requirement, first apply it in that project, then decide whether it should become a general
rule (step 7 of the workflow asks this). If so, change this page and the Chinese version
[`guide_cn.md`](guide_cn.md) together, record the reason in the workflow's
[`CHANGELOG.md`](../../CHANGELOG.md), and push.

- If your library points at your own copy of this repository (`durweg library list` shows its
  folder), the change takes effect at once.
- Everyone who installed the workflow from a catalog gets it with `durweg update` (or
  `durweg library update human-readme`).
- A run that has already started keeps the rules it started with: each run copies the workflow
  when it starts.

## 🔍 Before and after

MyTool below is made up; its commands, links and output only illustrate the structure.

**Bad** (features piled up; the reader does not know where to start):

````markdown
# MyTool
MyTool supports A, B, C, D, E and F, has five modules (core, io, cli, plugin, remote),
and options --foo --bar --baz ... (a 60-line option table)
## Install
pip / conda / docker / from source ... (15 lines each)
## Architecture
...
````

**Good** (four parts, details linked out):

````markdown
# MyTool
Turns medical image segmentations into editable 3D meshes, for clinicians and engineers
planning surgery.
![Input → output](docs/img/demo.png)

## Install and first run
Needs Python 3.10+ and git.

```bash
git clone https://github.com/you/mytool.git && cd mytool
pip install .
mytool convert examples/liver.nii.gz -o liver.stl
```

You should see `Saved liver.stl (12,345 faces)`. Other install methods: [install guide](docs/install.md).

## What you can do
- Convert a whole folder at once → [batch conversion](docs/batch.md)
- Export OBJ with label colours → [export formats](docs/export.md)
- [All features and options](docs/reference.md)

## Common problems
- `Unsupported file format`: [troubleshooting](docs/troubleshooting.md#formats)

[More docs](docs/) · [Ask a question](https://github.com/you/mytool/issues) · MIT
````

## 📚 Sources

- [The Good Docs Project README template](https://www.thegooddocsproject.dev/template/readme): section order, "be succinct", link out for details
- [Diátaxis](https://diataxis.fr/): four kinds of documentation, kept apart
- Art of README (noffle): "cognitive funneling", broad to specific
- [Google developer documentation style guide](https://developers.google.com/style/highlights), [Microsoft: writing step-by-step instructions](https://learn.microsoft.com/en-us/style-guide/procedures-instructions/writing-step-by-step-instructions): how to write sentences and steps
