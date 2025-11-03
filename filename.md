# filename related
## Inserting file name while in insert mode:
1. `ctrl`+`r`
2. `=expand('%')`
3. Then press enter

### Explannation
 * `%` is current file name
 * Modifers:
   * `:p` expand to full path. *Example:* `=expand('%:p')`
   * `:h` head (last path component removed)
   * `:t` tail (last path component only)
   * `:r` root (one extension removed)
   * `:e` extension only 
## Display
 * `:f` (`:file`) - Display filename
 * `<Ctrl>`+`G` - Display filename
## Rename
```bash
:saveas new_filename
```
**Exaplnation:**
 * `:saveas` saves the **current buffer's contents** to a new file (`new_filename`)
 * After this command, Vim **switches to editing the new file**.
 * The **old file**still exists - if we want to remove it, we have to delete it manually:
   ```bash
   :!rm %
   ```
   (**`%`** means ***the current file name***)
   

