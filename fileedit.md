# file edit
## Creating a New Buffer for Another File
## 1. Open a new buffer and name it immediately
```bash
:edit <file_name>
#or
:e <file_name>
```
"edit" the file $\rightarrow$ i.e., **open that file in the current buffer**.
**What `:e` or `:edit` does**
 * If the file exists $\rightarrow$ **open it** and load it into the current window (current buffer is replaced).
 * If the file does *not exist** $\rightarrow$ Vim opens an **empty buffer** with that name, ready to be saved later.
 * If the current file has unsaved changes $\rightarrow$ Vim will warn us (`E37`) unless we force it with:
```vim
:e! <file_name>
```

## 2. Open a new buffer in a split
### Horizontal split:
```bash
:split <file_name> 
# or
:sp <file_name> 
```

### Vertical split:
```bash
:vsplit <file_name>
# or
:vsp <file_name>
```

## 3. Open a new buffer in a new tab
```bash
:tabedit newfile.txt
```

## 4. Switching Between Bufferes
Once we have multiple buffers:

### List all buffers:
```bash
:ls
```
(or `:buffers`)

### Switch to buffer #2 (for example):
```bash
:buffer 2
```

### Use previous/next buffer:
```bash
:bp - previous buffer
:pn - next buffer
```

## Summary Sheet
|Command|Meaning|
|---|---|
|`:e file`|Open file in current window|
|`:sp file`|Open file in horizontal split|
|`:vsp file`|Open file in vertical split|
|`:tabedit file`|Open file in a new tab|
|||
|`:ls`|List buffers|
|`:b#`|Switch to previous buffer|
|`:bn`/`:bp`|Next / previous buffer|
|||
|`:Ex`|File explorer (netrw)|
|`:e .`|Open current directory in netrw|
|||
|`:mksession`|Save session|
|`:source`|Load session|
