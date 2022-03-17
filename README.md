# wine-disappearing-cursor-bug-fix
dirty hack to avoid any disappearing cursor bug in wine or anywhere else


compile libcursorfix.c as shared object like that

gcc -rdynamic -shared libcursorfix.c -o libcursorfix.so

then when launching your game.exe with wine just do

LD_PRELOAD="/home/a/libcursorfix.so" wine game.exe

and cursor will never disappear and never even update
