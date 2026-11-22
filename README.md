# nccl-daily-digest

每日检验科工作扫描结果（**仅数据，不含任何代码或密钥**）。

## 数据文件

- `data/latest.json` — 个人工作台「每日扫描提醒」卡片的数据源

## 更新方式

每天自动覆盖写入 3 次（北京时间 09:00 / 15:00 / 18:00），由私有仓库的 GitHub Actions 推送。

## 数据结构

```json
{
  "generated_at": "2026-11-22T14:10:31+08:00",
  "source": "combined_email.py",
  "blocks": [
    { "title": "板块名", "level": "alert|warn|ok|info",
      "items": [ { "text": "内容", "meta": "备注" } ] }
  ]
}
```

字段与「每日扫描提醒」对接需求单一致，无需鉴权即可读取。
