[English](README.md) · [中文](README_cn.md)

# human-readme

**A [Durweg](https://github.com/musetee/durweg) workflow that has AI agents write a project's README in 7 fixed steps, so that a first-time reader understands on the first screen what the project solves, picks the right way to install it and gets one example working.**

It was made with Durweg's own guide write-your-method, following the way the README of the AIagents
project was written, and then used to rewrite Durweg's own README. The whole story is on the
[case page](https://claude.ai/artifact/LGnCog4wnBmgMAWJg1Xmi4) (in Chinese; a copy is in this repository:
[case/human-readme.html](case/human-readme.html)). The workflow's texts are in Chinese.

## 🧭 Install

You need Durweg first ([install Durweg](https://github.com/musetee/durweg/blob/main/README.md)).

1. **Open a terminal** (as in step 1 of Durweg's "Every day").
2. **Add it to your library:** `durweg library add https://github.com/musetee/durweg-human-readme.git --name human-readme`.
   It downloads the workflow to `~/Durweg/workflows/human-readme/` and registers it. This needs git;
   without git, click **Code → Download ZIP** on GitHub, unzip it to a folder and run
   `durweg library add <that folder> --name human-readme`.

Done looks like this: it prints `added human-readme`, and `durweg library list` lists `human-readme`.

## 📅 Use it

Start your agent in the folder of the project whose README you write and tell it: "Run human-readme with durweg."

## 🪜 The 7 steps

| # | Step | Delivers | You decide |
| :--- | :--- | :--- | :---: |
| 1 | The core: the first sentence | The first sentence in Chinese and English, and why | ✅ |
| 2 | Readers and install entries | Readers, default path, one install line per kind of computer | |
| 3 | The front page skeleton | First drafts of README and README_cn | |
| 4 | Details off the front page | Pages under `docs/` and the links to them | |
| 5 | Walk it once | Where it was checked, the result, what was not checked | |
| 6 | You read it as a newcomer, it is fixed | Each remark, what changed, your words when satisfied | ✅ |
| 7 | General rules or not | The decision on each new request, and the files changed | ✅ |

## 🙋 I want to …

| I want to | How |
| :--- | :--- |
| See how this workflow was made | [case page](https://claude.ai/artifact/LGnCog4wnBmgMAWJg1Xmi4) |
| Make it my own | Make your own version with Durweg's write-your-method, or edit `workflow.json` and `skills/human-readme/SKILL.md` following the [workflow format](https://github.com/musetee/durweg/blob/main/docs/workflow-format.md) |
| Stop using it | `durweg library remove human-readme`, then delete `~/Durweg/workflows/human-readme/` |

---

License: [MIT](LICENSE).
