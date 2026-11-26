# Week 2：工具描述與分派觀察紀錄

## 1. 第一次 API 回應

HTTP status: 200

Tool name: http_get

Tool arguments:
{"url":"https://example.com"}

Tool call ID:
call-805a5ae2-aaba-412b-9fb9-4665eb253624

模型提出工具呼叫，但尚未執行。

## 2. Python 執行工具

執行函式：requests.get()

- status_code: 200
- body_summary: <!doctype html><html lang=en><head><meta charset=utf-8><link rel=icon href=data:,><meta name=viewport content="width=dev

## 3. 第二次 API 請求

role: tool

tool_call_id:
call-805a5ae2-aaba-412b-9fb9-4665eb253624

工具結果已回填，ID 與第一次 API 相同。

## 4. 第二次 API 回應

HTTP status: 200

最終回答：

抓取成功（HTTP 200），頁面是一個標準的 HTML 文件，包含 head 中的字元集與 viewport 設定等基本標記。

## 四列觀察表

| 步驟 | 模型建議 | 程式實際執行 |
|---|---|---|
| 第一次 API 回應 | http_get，URL: https://example.com | 尚未執行 |
| 工具執行 | 無 | status_code: 200，取得前 120 字 |
| 第二次 API 請求 | 無 | role: tool，tool_call_id 與第一次相同 |
| 第二次 API 回應 | 無 | 取得最終 content |
