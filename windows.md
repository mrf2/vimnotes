# Switching Between Windows and Editing Buffer and Help

### Splitting
 * **Hotizontal Splitting**
```bash
:split
```
***or***
```bash
:sp
```
 * **Cancel Horizontal Splitting**
```bash
<C-w> q
```
- Press ***Ctrl + w***, then press `q`
 * **Vertical Splitting**
```bash
:vsplit
```
 * **Cancel Vertical Splitting**
```bash
<C-w> q
```
- Press **Ctrl + w**, then press `q`
### Switching Between Editing Buffer and Help
 * Use `Ctrl-w` followed by `w`
```bash
<C-w> w
```
   * Press **Ctrl + w**, then press `w`.
   * This cycles through open windows.


## Using terminal inside window
```bash
:terminal           # this will split the window to show terminal
:close              # if the terminal open inside an existing split window,
                    # then close the other window
:Ctrl-\, Ctrl-n     # Exit terminal input mode
:i                  # Resume terminal input
```
