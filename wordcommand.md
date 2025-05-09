# Word-based commands
In Vim, the behavior of word-based commands like `dw` depends on what Vim considers a ***"word***. By default, `dw` stops at punctuation like `-`, so:
```bash
Example text: "hello-world"
dw --> deletes only hello in "hello-world"
```
To delete the whole `"hello-world"` including the quotes, we have to used text objeect commands
## To delete/cut `"hello-world"` including the quotes:
```bash
di"  --> delete inside the quotes (hello-world without enclosing double quotes)
da"  --> delete **a**round the quotes ("hello-world" delete with encosing double quotes) 

## `di"` --> Delete Inside Quotes
## `da"` --> Delete Around Quotes
## To work with other quote types
- `'`   $\rightarrow$   `di'`, `da'`
- `()`  $\rightarrow$   `di(` or `di)`, `da(`
- `{}`  $\rightarrow$   `di{`, `da{`
- `[]`  $\rightarrow$   `di[`, `da[` 


## The list of characters Vim considers part of a `"word"` is controlled by the `iskeyword`
- To view the current list:
```bash
:set iskeyword?
This will print something like:
```bash
iskeyword=@,48-57,_,192-255
```
    - `@` $\rightarrow$ all letters(a-z, A-Z)
    - `48-57` $\rightarrow$ ASCII digits (0-9), in hex 0x30 - 0x57
    - `_` $\rightarrow$ underscore is treated as part of words
    - `192-255` $\rightarrow$ extended Latin characters 
- To include something as part of word (example `-`):
```bash
:set iskeyword+=-
```
- To remove something from the parts of world (example `-`):
```bash
:set iskeyword-=-
```
