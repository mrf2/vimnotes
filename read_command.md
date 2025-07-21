# Read Command
`:r` or `:read`: It reads content from a file or shell command and inserts it  into the **current buffer**

## Examples
|Purpose|Command|Explanation|
|---|---|---|
|Read contents of a file|`:r filename.txt`|Inserts the contents of `filename.txt`|
|Read output from a shell command|`:r !ls`|Inserts the output of `ls` command|
|Read all subdirectories recursively|`:r !find . -type d`|
|Read all subdirectories absolute path Manually|`:r !find /my/full/path -type d`|Inserts all directores exists under `/my/full/path`| 
|Read all subdirectories absolute path Manually|`r !find /knowledge-base/development/python/Flask/ -maxdepth 1`|Inserts all directores exists under `/my/full/path`| 


## Advanced Use
 * Insert the **entire struct** `addrinfo` **definition** from the man page
```bash
:r !man getaddrinfo | col -b | sed -n '/struct addrinfo {/,/};/p'
```

```bash
:r !man getaddrinfo | col -b | awk '/struct addrinfo {/,/};/'
```

## Insert mode:
```bash
<C-r>=system('man socket | col -b| grep "int socket(.*);"')<CR>
```

