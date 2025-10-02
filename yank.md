# yank (copy)

 * yank (copy) from the **current cursor position** to the **end of the line**, we can use:`y$`
 * Breakdown:
   * `y` $\rightarrow$ yank (copy)
   * `$` $\rightarrow$ motion that moves the cursor to the end of the current line

 * If we only want to yank a few words, we could use:
   * `yw` $\rightarrow$ yank one word
   * `2yw` or `y2w` $\rightarrow$ yank two words
   * `yE` $\rightarrow$ yank to the end of the current word (*including punctuation*)
   * `y}` $\rightarrow$ yank to end of paragraph
   * `yG` $\rightarrow$ yank until end of file


### Example selecting and copying 5 lines from current lines
```bash
   :.,+5y
```
