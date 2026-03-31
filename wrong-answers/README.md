# wrong-answers

这个目录用于存放刷题网页导出的错题文件，作为后续二次出题的素材池。

## 约定

- 优先保存 `json` 文件，便于程序读取并自动生成新题
- 文件名建议格式：
  - `wrong-answers-YYYYMMDD-HHmmss.json`
- 如需人工查看，也可同时保留对应的 `.md` 文件

## 推荐流程

1. 在刷题网页点击“导出错题包（JSON+Markdown）”
2. 浏览器下载本地文件
3. 把下载的 `.json` 或 `.zip` 发给我，或手动提交到本目录
4. 之后你说“基于错题再出一套题”时，我优先读取本目录里的历史错题文件

## JSON 结构

```json
{
  "version": 1,
  "exportedAt": "2026-03-31 10:30:00",
  "source": {
    "site": "审计数据采集与神通数据库刷题页",
    "note": "审计数据采集与神通数据库学习笔记-2026-03-30"
  },
  "summary": {
    "wrongCount": 2,
    "totalQuestions": 10
  },
  "wrongs": [
    {
      "id": 2,
      "tag": "聚合倍增",
      "question": "两张明细表发生 N 行匹配 M 行后，再直接 GROUP BY 聚合，最容易出现什么问题？",
      "selected": "聚合结果不受影响",
      "correct": "聚合结果被重复放大",
      "explanation": "连接结果会被放大，后续聚合可能失真。"
    }
  ]
}
```
