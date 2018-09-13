# Quickfix list

## Building

Command | Keystrokes | Comments
------- | ---------- | --------
Run make (and jump to first error, if there are any) | `:make`
Run make (and stay where we are) | `:make!` | if you forgot and have moved, you can use `<c-o>`

## Show and Hide

Command | Keystrokes | Comments
------- | ---------- | --------
Open quickfix window | `:copen`
Move from one window to another | `<c-w>j`, `<c-w>k`
Close quickfix window | `:cclose`
Close quickfix window *when it is active* | `:q`

## Navigating Quickfix list

Command | Keystrokes | Comments
------- | ---------- | --------
Move to next error in quickfix list | `:cnext`
Previous | `:cprev`
Move forward five items | `:5cnext`
Move back five items | `:5cprev`
First | `:cfirst`
Last | `:clast`
First item in next file | `:cnfile`
Last item in previous file | `:cpfile`
Nth item | `:cc N`

## See previous quickfix list results

Command | Keystrokes | Comments
------- | ---------- | --------
See older version | `:colder` | also takes a count (e.g. `:5colder`)
See newer version | `:cnewer` | also takes a count

## Set a different make program

Command | Keystrokes | Comments
------- | ---------- | --------
For example, list the current file | `:setlocal makeprg ls\ -alF\ %` | Note that spaces are escaped - see `:help makeprg` for more info
