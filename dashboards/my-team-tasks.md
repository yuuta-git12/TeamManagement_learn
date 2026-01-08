
# 🔥 対応中（Doing）
```dataview
table backlog_key as "Key", title as "タスク", priority as "優先度", due as "期限",担当者
from "tasks"
where type = "task"
  and team = "my-team"
  and status = "処理中"
sort due asc
```

# 📝 未着手（Todo）

```dataview
table backlog_key as "Key", title as "タスク", priority as "優先度", due as "期限",担当者
from "tasks"
where type = "task"
  and team = "my-team"
  and status = "未着手"
sort priority desc, due asc
```

# ✅ 完了（Done）

```dataview
table backlog_key as "Key", title as "タスク", due as "期限",担当者
from "tasks"
where type = "task"
  and team = "my-team"
  and status = "処理済"
  or status = "PR済"
  or status = "STG済"
sort due desc
```

