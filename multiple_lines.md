# Working with multiple lines - yanking (copying), deleteing, indenting etc.

## Yank 5 lines
```bash
   5yy
```

## Line Range
|Sysmbol|Meaning|
|:---:|---|
|`.`|Current line|
|`$`|Last line|
|`1`|First Line|
|`+n`|`n` lines **after** current line|
|`-n`|`n` lines **before** current line|

### Deleting all lines from the current line (.) up the the defined line:
```bash
   :.,25d
```
 - `:` - Enters command-line mode.
 - `.` - Current line.
 - `,` - Comma is used for define range, here current line (.) to line number 25
 - `25` - Absolute line number.
 - `d` - Delete.
This will delete a **continous block of lines** starting from where our cursor is now, up to line 25.

### Example selecting and copying 5 lines from current lines
```bash
   :.,+5y
```
Now paste it by pressing `p` key in **command** mode


### Comment out multiple lines
```bash
   :.,$normal I#
```

 - `:` - Enters command-line mode.
 - `.` - Current line.
 - `,` - Comma is used for define range, here current line (.) to end of file
 - `$` - All lines from the current line
 - `normal` - Normal mode
 - `I#` - Insert # at the beginning of each line

### Adding something to multiple lines
```vim
:10,50normal! I<sometext>
```
 * `10,50` $\rightarrow$ Line range
 * 
