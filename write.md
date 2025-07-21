# `:w` - write (save) the current buffer (file) to disk.

## Related Concepts
 * **Buffer:** Vim's in-memory representation of a file.
 * **Write:** Copies the buffer content to disk.
 * **Modified flags:** Vim tracks whether a buffer has changed 

### Command
|Command|Action|
|---|---|
|`:w`|Write to *current file*|
|`:w filename.txt`|Write buffer to *new filename*|
|`:w!`|Force write (e.g., read-only file|
|`:w >> file.txt`|Append buffer content to existing file|
|`:w %`|Write to the file currently being editd (same as `:w`)|
|`:wq`|Write and quit|
|`:x` or `ZZ`|Save and quit (only if changed)|
 
