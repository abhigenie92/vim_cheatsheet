# vim_cheatsheet

Vim CheatSheet: (From vimtutor)
`
↓ j   k ↑
← h  l → 
`

`vim <filename>`

1. **Saving Options**:
    1. `<ESC> + q!` : exits the editor discarding any changes
    2. `<ESC> + wq `: save a file and exit.
    3. `<ESC> `: place in Normal mode/cancel unwanted partially completed commands
    4. `<ESC> + w <filename> `: save with filename
2. **Insert mode**:
    1. `i` : insert text
    2. `a` : insert text after the cursor.
    3. `A` : insert text at end of the line
    4. `o` : open a line below the cursor and place you in Insert mode
    5. `e` : moves to the end of a word
3. **Delete** :  commands that change text: operator motion
    1. `dw` : delete a word
    2. `d$` : delete to the end of the line
    3. `x` : delete the character under the cursor
4. **Motions**:  just the motion in Normal Mode without an operator will the move the cursor as specified
    1. Single motion:
        1. `w` : until the next word, excluding the first character
        2. `e` : to the end of the current word, including the last character; ex - de delete from the cursor to the end of the word]
        3. `$` : to the end of line, including the last character
    2. Multiple Motion:  typing a number with an operator repeats it that many times;                       
        1.  number motion :
            1. `2w` : move two words forward
            2. `3e` : move the cursor to the end of third word forward
            3. `0` : move to the start of the line
        2. operator [number] motion :
            1. `d2w` : delete two words
        3.  others:
            1. `dd` : delete whole line
            2. `2dd` : delete two lines
5. **Undo/Redo**:
    1. `u` : undo last commands
    2. `U` : undo changes in the whole line
    3. `CTRL+R` : redo
    4. `p` : to put previously deleted text after cursor
6. **Replace mode**: Every typed character deletes a existing character.
    1. Replace a character:
        1. `r<x>`: to replace the character at the cursor with x
    2. Replace mode:
        1. `R` : enters Replace mode until <ESC>.
7. **Change**: 
    1. `c [number] motion`:
        1. `ce` : deletes the word and places you in Insert mode
        2. `c$` : deletes till the end of line and places you in Insert mode
8. **Cursor movement across lines**:
    1. `G` : to move to the bottom of the file
    2. `gg` : to move to the start of the file 
    3. `<line number>+G` : move to the line number mentioned
    4. `CTRL+G` : show location in the file and status
9.  **Search**:
    1. `/ + <phrase>` : search for phrase
        1. `n` : search for same phrase again.
        2. `N` : search for same phrase in opposite direction.
        3. `CTRL+O` : go back where you came from
        4. `CTRL+I` : goes forward
        5. `\c` : at the end after the phrase ignores case. 
    2. Set Options: 
        1. `:set ic` : Ignore case while searching, reverted by :setnoic
        2. `:set hls` :highlights matches
    3. Matching parentheses search:
        1. `%` : to find a matching ),], or } and toggle between the 2.
10. **Replace**:
    1. `:s/old/new` : to replace the old with new for first occurrence
        1. `:#,#s/old/new/g` : where #,# are the line numbers of the range of lines where the substitution is to be done.
        2. `: %s/old/new/g` : to change every occurrence in the whole file.
        3. `:%s/old/new/gc` : to find every occurrence in the whole file, with a prompt whether to substitute or not.
11. **Execute command**:
    1. `:!<command>` : followed by an external command to execute that command.
        1. `:!ls` :  to get a listing of your directory
        2. `!rm <filename>` : remove the file
12. **Parts of file**:
    1. Saving a part of file:
        1. `v  motion  :w <filename>` : saves the Visually selected lines in file. ('<,'> appear on : in visual mode.)
    2. Inserting file/command:
        1. `:r FILENAME` : retrieves disk file FILENAME and puts it below the cursor position.
        2. `:r !<command>` :  reads the output of the dir command and puts it below the cursor position.
13. **Copy/Paste**: Start Visual mode with v
    1. `y` : to copy the highlighted text.
    2. `d` : to cut highlighted text.
    3. `yw` : copy one word (Normal mode)
    4. `p` : to put(paste) the text 



TODO:
1.Toggle comments.
2. Page down/up 

https://gist.github.com/jonlabelle/11053123
