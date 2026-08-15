![Adapt Explanation](assets/social-preview.png)

# Adapt Explanation

把任何事情解釋給任何人聽，同時保留真正重要的資訊。

`adapt-explanation` 是一個適用於 Codex 與 ChatGPT 的開放 agent-skill 專案。安裝後的 skill 特意使用簡短名稱 `explain`，方便快速呼叫；它會依照讀者的年齡、專業程度、角色、目的、語言、語氣與深度調整說明方式，而不是單純把內容縮短或幼兒化。

**專案：** `adapt-explanation` · **Skill：** `explain` · **呼叫方式：** `$explain`

[English](README.md) · [Prompt 範例](examples/prompt-gallery.md) · [Skill 指令](skills/explain/SKILL.md)

## 它能做什麼？

- 分別向小朋友、初學者、實作者、專家或主管解釋同一件事。
- 同時提供簡單版與技術版。
- 改寫原始內容，但不憑空增加主張或刪除重要限制。
- 保留指令、程式識別字、API 欄位、公式、引用與警告。
- 簡化醫療、法律、金融、安全內容的語言，而不是簡化必要保障。
- 依照使用者要求的語言回答。

## 快速安裝

在 Codex 中輸入：

```text
Use $skill-installer to install the explain skill from:
https://github.com/KevinAbura/adapt-explanation/tree/main/skills/explain
```

安裝後明確呼叫：

```text
$explain 請用五歲小朋友能理解的方式解釋 Kubernetes。
```

當請求符合 skill 的描述時，Codex 也能自動啟用它。

## 可以直接試用的 Prompt

```text
$explain 請分別向五歲小朋友、後端初學者和 CTO
解釋 Kubernetes，每個版本不超過 120 字。
```

```text
$explain 請把這份 API 文件改寫給剛入職的後端工程師，
所有指令和 JSON 欄位必須保持完全相同。
```

```text
$explain 請把這項架構決策分成主管版與資深工程師版。
```

更多內容請查看 [Prompt 範例](examples/prompt-gallery.md)。

## 設計原則

這個 skill 會先判斷受眾與目的，再確認哪些事實、風險和限制不能因簡化而消失。接著才調整詞彙、例子、結構和細節，最後檢查內容是否清楚、實用且沒有誤導。

主要流程位於 [`SKILL.md`](skills/explain/SKILL.md)，受眾設定位於 [`audience-profiles.md`](skills/explain/references/audience-profiles.md)。

## 授權

MIT © Kevin Abura
