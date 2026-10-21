# 台灣裁判書研究

依法律爭點與關鍵字搜尋司法院裁判，核對官方全文，整理裁判理由、比較與可追溯引用。這是一個 Agent Skill，支援 Codex、Claude Code、Cursor 等可安裝 Agent Skills 的工具；不需 API 金鑰或第三方 MCP。

## 安裝

需要 Node.js / npm。使用 [Agent Skills CLI](https://github.com/vercel-labs/skills) 安裝到所有支援的 Agent：

```bash
npx skills add AndyJuang/taiwan-judgment-research --skill taiwan-judgment-research --global --agent '*' --yes
```

只安裝到 Codex：

```bash
npx skills add AndyJuang/taiwan-judgment-research --skill taiwan-judgment-research --global --agent codex --yes
```

安裝後重新開啟 Agent 工作階段，或明確呼叫 `$taiwan-judgment-research`。安裝只加入工作流程指引；搜尋時仍須能連線查詢司法院網站。

## 使用範例

> 搜尋最高法院近三年對詐欺罪不確定故意的裁判，整理法院理由並附官方原文連結。

## 資料來源與範圍

- 日常關鍵字檢索以[司法院裁判書查詢系統](https://judgment.judicial.gov.tw/FJUD/default.aspx)為準，每一項分析都應回到官方裁判全文核對。
- 司法院[裁判書開放 API](https://opendata.judicial.gov.tw/api/Newses/42/file)提供裁判異動清單與依 JID 取得全文，並非任意關鍵字搜尋服務。
- 本 Skill 整理公開裁判資料，不代替律師對個案提供法律意見；檢索結果亦不保證涵蓋所有相關裁判。

## 內容

- `SKILL.md`：檢索、原文核對、引用及比較流程。
- `agents/openai.yaml`：Codex 顯示名稱與預設提示。
