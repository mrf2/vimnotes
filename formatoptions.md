# Vim formatoptions

### Help Menu
```bash
:help formatoptions
```
## Check current `formatoptions`
To see wich are currently active:
```vim
:set formatoptions?
```

## Customizing `formatoptions`
|Action|Command|
|---|---|
|Remove flags|`:set formatoptions-=r`|
|Add flags|`:set formatoptions+=t`|
|Set exact flags|`:set formatoptions=tcq`|

## Example
 * Disable Comment Continuation
```vim
:set formatoptions-=cro
```
This **removes** `c`, `r`, and `o` from `formatoptions`.

## `formatoptions` Flags
|Flag|Description|
|---|---|
|`t`|Auto-wrap text using `textwidth` (normal text, not comments)|
|`c`| Auto-wrap comments using `textwidth`|
|`r`|Automatically insert comment leader when pressing `Enter`|
|`o`|Automatically insert comment leader when using `o` or `O`|
|`q`|Allow `gq` to format comments|
|`n`|Recognize numbered lists for formatting|
|`2`|Use second line's indent for formatting|
|`1`|Don't break a line after a one-letter word (e.g., "a", "I")|
|`a`|Auto formatting: as we type or paste text, it's formatted automatically|
|`w`|Trailing whitespace indicates paragraph continues|
|`b`|Don't join lines with `gq` if they are comment lines with different leaders|
|`l`|Long lines are not broken in insert mode|
|`m`|Keep mail headers (e.g., ">") when formatting|
|`j`|Remove comment leader when joining lines|
|`v`|Only break at spaces when formatting (no hyphen splits)|
|`p`|Dont' break lines in quoted text|
|`y`|Preserve empty lines when formatting|
|`#`|Recogize comments strting with `#` as special|


## Comment Leader
Vim uses the **comment leader** to:
 * **Countinue comments automatically** (if `formatoptions` has `r` or `o`)
 * **Recognize comment blocks for formatting (`gq` with `q` flag)
 * **Handle joining lines cleanly** with (`j` flag - removes leader when joining)

