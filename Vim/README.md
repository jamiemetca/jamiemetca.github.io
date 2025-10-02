01/02/2025

# Vim

## Explore mode
Open vim in Explorer mode
```vim
vim .
```

Open explorer
```vim
:Ex
```

Open explorer by spliting the screen vertically
```vim
:Vexplore
```

Open explorer by spliting the screen horizontally
```vim
:Hexplore
```

Explore commands
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
