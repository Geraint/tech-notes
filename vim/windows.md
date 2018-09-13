# Windows

For another excellent tutorial, see http://reefpoints.dockyard.com/2013/11/27/vim-windows.html

## Split Windows

Operation | Keystrokes
--------- | ----------
split current window | `<c-w>s`
split current window vertically | `<c-w>v`
close current split | `<c-w>q`

Note that, as in all of these examples `<c-w>s` is the same as `<c-w><c-s>`, which might be easier to type repeatedly.

## Select window

Operation | Keystrokes
--------- | ----------
switch to window to left | `<c-w>h`
switch to window to right | `<c-w>l`
switch to window above | `<c-w>k`
switch to window below | `<c-w>j`

## Move/Rotate windows

Operation | Keystrokes
--------- | ----------
rotate windows | `<c-w>r`
rotate windows (opposite direction) | `<c-w>R`
move current window the far left and use the full height of the screen | `<c-w>H`
move current window the far bottom and use the full width of the screen | `<c-w>J`
move current window the far top and full width of the screen | `<c-w>K`
move current window the far right and full height of the screen | `<c-w>L`

## Resize Windows

Operation | Keystrokes | Comment
--------- | ---------- | -------
resize the windows equally  | `<c-w>=`
incrementally increase the window to the right | `<c-w>>` | takes a parameter, e.g. `<c-w>20>`
incrementally increase the window to the left | `<c-w><` | takes a parameter, e.g. `<c-w>20<`
incrementally decrease the window's height | `<c-w>-` | takes a parameter, e.g. `<c-w>10-`
incrementally increase the window's height | `<c-w>+` | takes a parameter, e.g. `<c-w>10+`

