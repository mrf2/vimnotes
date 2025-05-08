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
