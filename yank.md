# yank (copy)

 * yank (copy) from the **current cursor position** to the **end of the line**, we can use:`y$`
 * Breakdown:
   * `y` $\rightarrow$ yank (copy)
   * `$` $\rightarrow$ motion that moves the cursor to the end of the current line

 * If we only want to yank a few words, we could use:
   * `yw` $\rightarrow$ yank one word
   * `2yw` or `y2w` $\rightarrow$ yank two words
   * `yE` $\rightarrow$ yank to the end of the current word (*including punctuation*)
   * `y}` $\rightarrow$ yank to end of paragraph
   * `yG` $\rightarrow$ yank until end of file

## Yank **single character**
### 1. Using Motion
If our cursor is on the chracter we want to yank:
```bash
yl
```
 * `y` $\rightarrow$ yank command
 * `l` $\rightarrow$ move one character right
```

### 2. Using Visual Mode
```bash
v
l
y
```
 * `v` $\rightarrow$ start visual selection
 * `l` $\rightarrow$ move right one character
 * `y` $\rightarrow$ yank the selection

### 3. Yank into a Named Register
If we want to save it into a specific register, e.g. `a`:
```bash
"ayl
```
Then later paste it with:
```
"ap
```

### 4. Yank backward (previous character)
```bash
yh
```

## Yank **a Specific Number of Characters (Forward)**
### 1. Yank **a Specific Number of Characters (Forward)**
We can combine **`y` + Count + Motion**
For Example;
|Command|Meaning|
|`yl`| Yank 1 character (current one)|
|`2yl` or `y2l`| Yank 2 characters (current + next)|
|`5yl` or `y5l`| Yank 5 characters forward|
|`10yl` or `y10l`| Yank 10 characters forward|

So, in general form:
```bash
[count]yl
or
y[count]l
```


## Yank from **cursor position to nth word** or **from cursor to specific character (like until `;`)**


```bash
### Example selecting and copying 5 lines from current lines
```bash
   :.,+5y
```


### Paste something multiple times using a ***count***
If we already yanked something, for examples, *a single character with* **`yl`** or *multiple characters with* **`y5l` or `5yl`**, then, then  we can paste in **N times** using:
```vim
[count]p
```
#### Examples:
|Command|Meaning|
|---|---|
|`p`|Paste once|
|`5p`|Paste 5 times|
|`20p`|Paste 20 times|

So if we yanked a single char `a`, then:
```vim
20p
```

$\rightarrow$ pastes it 20 times after the cursor.  
