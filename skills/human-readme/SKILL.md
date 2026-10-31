---
name: human-readme
description: 写给人看的 README - the user's own method, run step by step with Durweg.
---

# 写给人看的 README

Run it with durweg (skill run-workflow): `durweg start human-readme <name-of-this-run>`, then for each step `durweg begin`, do the step, write its file, and `durweg done`. Talk to the user in the language set in ~/Durweg/config.json.

## 1. core

**定核心：第一句**

Do: 读项目代码和现有文档，用一句话写出核心价值和它解决的问题（不讲故事，不罗列功能），中英各一句

Deliver: steps/1-core.md：第一句的中文和英文，以及依据

Write `steps/1-core.md` with a `## Result` section that holds what this step delivered.

The user decides here: write the result, `durweg propose`, show it to the user, and `durweg confirm` with their own words when they agree.

## 2. readers

**定读者和安装入口**

Do: 默认写给第一次用的人；列出读者会用的电脑，每种一行安装入口，写明容易混的情况（如 Windows 里的 WSL）走哪一行

Deliver: steps/2-readers.md：读者、默认路径、每种电脑一行的入口表

Write `steps/2-readers.md` with a `## Result` section that holds what this step delivered.

## 3. skeleton

**搭首页骨架**

Do: 写 README 和 README_cn：安装（只写安装）、每天怎么用（编号小步，第一步写怎么打开终端）、文件在哪里、案例（第一句说展示什么、做出什么）、我想……、末尾说明列表；没内容的节不建

Deliver: README.md 和 README_cn.md 的初稿

Write `steps/3-skeleton.md` with a `## Result` section that holds what this step delivered.

## 4. details

**把细节移出首页**

Do: 分步安装、特殊地区、卸载、参数和命令全表等各放一页（中英两版），首页每项只留一句加链接；检查本地链接和锚点

Deliver: docs/ 下的子页面，以及首页里指向它们的链接

Write `steps/4-details.md` with a `## Result` section that holds what this step delivered.

## 5. walkthrough

**实际走一遍**

Do: 在新电脑或新 WSL 上照着首页从头做到案例成功，遇到不对的地方先改步骤

Deliver: steps/5-walkthrough.md：在哪里验证、每一步的结果、哪些没验证

Write `steps/5-walkthrough.md` with a `## Result` section that holds what this step delivered.

## 6. review

**用户以新手眼光读并改**

Do: 请用户读首页，一条一条提意见；中英文一起改，一次改一件事；直到用户满意

Deliver: steps/6-review.md：每条意见、改了什么（提交号），以及用户满意的原话

Write `steps/6-review.md` with a `## Result` section that holds what this step delivered.

The user decides here: write the result, `durweg propose`, show it to the user, and `durweg confirm` with their own words when they agree.

## 7. rules

**决定要不要变成通用规则**

Do: 对每条新要求问用户要不要变成通用规则；要的话同时更新 human-docs（中英文和精简版），在 CHANGELOG 写明原因

Deliver: steps/7-rules.md：每条要求的决定，以及改动的文件

Write `steps/7-rules.md` with a `## Result` section that holds what this step delivered.

The user decides here: write the result, `durweg propose`, show it to the user, and `durweg confirm` with their own words when they agree.
