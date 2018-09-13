# File Explorer

## Open (and close) a file explorer

### Current Directory

Operation | Keystrokes | Shortcut
--------- | ---------- | --------
start exploring (from project root)                              | `:ex .`     | `:e.`
open explorer pain in split (project root)                       | `:split .`  | `:s.`
open explorer pain in vertical split (project root)              | `:vsplit .` | `:vs.`

### Project Root Directory

i.e. the project you opened n?vim in.

Operation | Keystrokes | Shortcut
--------- | ---------- | --------
start exploring (from directory of current file)                 | `:Explore`  | `:Ex`
open explorer pain in split (directory of current file)          | `:Sexplore` | `:Sex`
open explorer pain in vertical split (directory of current file) | `:Vexplore` | `:Vex`

## Close file explorer

Operation | Keystrokes
--------- | ----------
close current split  | `<c-w>q`
close current buffer | `:bd`

## Move around

Operation | Keystrokes
--------- | ----------
go up one directory | `-`

## View settings

Operation | Keystrokes
--------- | ----------
Cycle through view types           | `i`
Permanently set this in `~/.vimrc` | `let g:netrw_liststyle=3`
Hide banner                        | `I`
Permanently set this in `~/.vimrc` | `let g:netrw_banner=0`

## Create files and folders in current directory in a file explorer

Operation | Keystrokes
--------- | ----------
Create file | `%`
Create directory | `d`
Rename | `R`
Delete | `D`

