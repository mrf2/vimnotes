# Searching

### Searching and replace
```bash
   :g/pattarn/s/old/new/g
   :g/,/s///g
```

### Find all filenames matching xxxx-yyyy.jpg and replace them
```bash
   :%s/\(\k\+\-\k\+\.jpg\)/asset\/\1/g
```
Command explanation:
|Part|Meaning|
|---|---|
|`%s/.../.../g`|Substitute in **all lines,** globally|
|`(\k\+\-\k\+\.png\)`|Capture the filename (e.g., `file-name.jpg1`)|
|`\k`|Matches a "keyword" character (like `[a-zA-Z0-9_]`)
|`\+`|Means "one or more"|
|`\asset\/\1`|Insert `asset/` followed by the match (`\1`)|
