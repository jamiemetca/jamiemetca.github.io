[Home](/)

01/10/2025

# Vim

## Update VIMRC
:e $MYVIMRC - Will open your vimrc
:so ~/.vimrc - will source and apply the changes

## Explore mode
### Open vim in Explorer mode
```vim
vim .
```

### Open explorer
Adding ! to the end of the command opens explorer in the right window.

```vim
:Ex
:Ex!
```

### Open explorer by spliting the screen vertically
```vim
:Vexplore
```

### Open explorer by spliting the screen horizontally
```vim
:Hexplore
```

### Explore commands
d - creates a directory
% - creates a file
R - Rename file
D - Delete file

## Tabs
:tabnew - Open new blank tab
:tabedit [filename] open file in tab (I haven't got this to work relatively yet
gt - next tab
gT - previous tab
[i]gt - go to tab i
:tabs - list tabs
:tabm 0 - move current tab to first position
:tabm - move current tab to last position
:tabc - close current tab
:tabo - close all other tabs

## Splits
:close - closes current split

## Term
:term bash - will launch a terminal split
- Close terminal
    exit - marks the session as finished
    - Both :q and :close close the split

## Digraphs
Symbols which cannot be easily typed.

To show a list of digraphs
```vim
:dig!
```
- micro
My = µ

- ohms

W* =  Ω

- Degrees

DG = °

To enter a digraph.
- While in insert mode.
- Type ctrl-k
- Followed by the two character code.

## Numbered bullet points
Use cat to add numbers to the start of specific lines.
In visual mode, highlight the rows.

```vim
:'<, '>!cat -n
```
The part between the colon and exclaimation mark will be added automatically.
This part: '<, '>

## Column movement
To jump to a column position
```vim
80|
```
