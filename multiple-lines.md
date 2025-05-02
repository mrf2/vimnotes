# Working with multiples line - yanking (copying), deleteing, indenting etc.

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

### Example selecting and copying 5 lines from current lines
```bash
   :.,+5y
```
Now paste it by pressing `p` key in **command** mode
