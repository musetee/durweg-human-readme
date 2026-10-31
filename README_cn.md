[English](README.md) · [中文](README_cn.md)

# human-readme

**一个 [Durweg](https://github.com/musetee/durweg) 工作流：让 AI agent 按固定的 7 步给项目写 README，第一次来的人能在第一屏看懂项目解决什么问题、选对安装路线、跑通一个案例。**

它是用 Durweg 自带的引导 write-your-method 做出来的；做出来以后，用它重写了 Durweg 自己的 README。整个过程见[案例网页](https://claude.ai/artifact/LGnCog4wnBmgMAWJg1Xmi4#zh)（中英文可以切换，默认英文；本仓库里也有一份：[case/human-readme.html](case/human-readme.html)）。

## 🧭 安装

需要先装好 Durweg（[安装 Durweg](https://github.com/musetee/durweg/blob/main/README_cn.md)）。

1. **打开终端**（和 Durweg 的“每天怎么用”第 1 步一样）。
2. **装进方法库：** `durweg library add https://github.com/musetee/durweg-human-readme.git --name human-readme`。它会把工作流下载到 `~/Durweg/workflows/human-readme/` 并登记。需要电脑上有 git；没有 git 的话，在 GitHub 页面点 **Code → Download ZIP**，解压到一个文件夹，再运行 `durweg library add <那个文件夹> --name human-readme`。

看到 `added human-readme`，并且 `durweg library list` 里有 `human-readme`，就装好了。

## 📅 怎么用

在要写 README 的项目文件夹里启动 agent，对它说：“用 durweg 运行 human-readme”。

## 🪜 7 个步骤

| # | 步骤 | 交出什么 | 由你决定 |
| :--- | :--- | :--- | :---: |
| 1 | 定核心：第一句 | 第一句的中英文和依据 | ✅ |
| 2 | 定读者和安装入口 | 读者、默认路径、每种电脑一行的入口表 | |
| 3 | 搭首页骨架 | README 和 README_cn 的初稿 | |
| 4 | 把细节移出首页 | `docs/` 下的子页面和首页里的链接 | |
| 5 | 实际走一遍 | 在哪里验证过、结果、哪些没验证 | |
| 6 | 你以新手眼光读，并修改 | 每条意见、改了什么、你满意的原话 | ✅ |
| 7 | 决定要不要变成通用规则 | 每条新要求的决定和改动的文件 | ✅ |

## 🙋 我想……

| 我想 | 怎么做 |
| :--- | :--- |
| 看这个工作流是怎么做出来的 | [案例网页](https://claude.ai/artifact/LGnCog4wnBmgMAWJg1Xmi4#zh) |
| 改成自己的写法 | 用 Durweg 的 write-your-method 做一个自己的版本；或者照 [工作流格式](https://github.com/musetee/durweg/blob/main/docs/workflow-format_cn.md) 改 `workflow.json` 和 `skills/human-readme/SKILL.md` |
| 不用了 | `durweg library remove human-readme`，再删掉 `~/Durweg/workflows/human-readme/` |

---

MIT 许可证：[LICENSE](LICENSE)。
