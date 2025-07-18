# Debugging

## Debug: Confirm the syntax region
Move cursor to the problematic area and type:
```bash
:echo synIDattr(synID(line('.'), col('.'), 1), 'name')
```
This will show the name of the current syntax region, like `markdownItalic`
