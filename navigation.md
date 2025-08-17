# Navigation to line, word, characters, paragraph etc.
 - Go to a specific character position (i.e. column number) in the current line: `{N}|`
 - Go to last cursor position `''`

## Go to the next/previous occurrence of current word which in where cursor is focusing
- Press `*` for the next occurrence of the current word
- Press `#` for the previous occurrence of the current word

## Word and Block Movements
 * *"word"* = letters/digits/underscore
 * *"WORD"* = any non-blank string
|Command|Description|
|---|---|
|`w`|Next **start of word**|
|`W`|Next **star of WORD** *(non-whitespace word)*|
|`e`|End of word|
|`E`|End of WORD|
|`b`|Back to beginning of WORD|
|`B`|Back to beginning of WORD|
|`ge`|Back to **end** of previous word|

