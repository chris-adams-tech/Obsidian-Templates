The below table will query your Daily notes from the past 7 days and show the stats (completed/not completed).
```dataview
table
  medicine as "🍃 Medicine", 
  push-ups as "💪 Push-ups", 
  write as "✍️ Write", 
  running as "🏃 Running", 
  apply-for-2-jobs as "📋 Apply Jobs" 
FROM "Personal/Daily Notes" 
WHERE file.day <= date(now) AND file.day >= date(now) - dur(7 days) SORT file.day ASC
```


> [!info] Technical Documentation
> For more information regarding Dataview structure and types, see here: https://blacksmithgu.github.io/obsidian-dataview/

