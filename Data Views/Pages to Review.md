Use the below table to review any pages before publishing. This uses the `draft: - []` checkbox in *Properties* in order to keep the note private. When the box is checked, the note will note be included *Published* content.

```dataview
table title as "Title", summary as "Summary", created as "Date", tags as "Tags"
from "articles"
sort desc
```

This is just an example, and in the `from` line, you will need to indicate the path to the directory you are wanting to pull from.

> [!info] Technical Documentation
> For more information regarding Dataview structure and types, see here: https://blacksmithgu.github.io/obsidian-dataview/
