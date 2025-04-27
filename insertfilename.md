## Inserting file name while in insert mode:
1. `ctrl`+`r`
2. `=expand('%')`
3. Then press enter

## Explannation
`%` is current file name

## Modifers:
`:p` expand to full path. *Example:* `=expand('%:p')`

`:h` head (last path component removed)

`:t` tail (last path component only)

`:r` root (one extension removed)

`:e` extension only 
