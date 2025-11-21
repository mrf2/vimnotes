# insert.md
We can add text in front of multiple lines at once in **Vim** using **Visual Block Mode** or a **substitution command**. Below are two methods:

## Method 1: Visual Block Mode
 1. Go to first line from where you want to start something like **bullet, space, tab, etc**
 2. Press `Ctrl-v` to enter **Visual Block Mode**
 3. Use `j` or `↓` to select all desired lines
 4. Press `I` (capital i) to go into insert mode
 5. Type `*` or `-` or `+`, `<space`>, `<your desired text>` (whatever we want)
 6. Press `Esc`

✅ Vim will insert the desired text on all selected lines 

## Method 2: **`:normal`** command (Powerful and Scriptable)
If the lines are, for example, from 20 to 57:

```vim
:10,57normal! I*
```
**Explanation:**
 * `10,59` $\rightarrow$ Line range
 * `normal!` $\rightarrow$ Run normal mode commands
 * `I*` $\rightarrow$ Insert `*` at the beginning of each line


