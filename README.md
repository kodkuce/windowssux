# windowssux
Making windows 10 bahave more like linux Rofi + Openbox kinda

**Win + 1 2 3 4** , switches betwin difrent workspaces 

**Win + R** , lounches Rofi alternative ueli

**Win + F1** , make selected window stick on top


* get desktopswitcher
https://github.com/isobit/win10-desktop-switcher

* get movetodesktop, for easyer workspace swaping
https://github.com/Eun/MoveToDesktop

* get autohotkeys
https://github.com/Lexikos/AutoHotkey_L/tree/alpha

* get ueli, rofi like alterantive
https://github.com/oliverschwendener/ueli

* get flameshot, screenshoting app
https://github.com/flameshot-org/flameshot

* get nice image viwer
https://github.com/nomacs/nomacs


* Create autohotkey scripts:

SwitchDesktops.ahk 
```
#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.

LWin::return

LWin & 1::Run, DesktopSwitcher.exe 0, , hide
LWin & 2::Run, DesktopSwitcher.exe 1, , hide
LWin & 3::Run, DesktopSwitcher.exe 2, , hide
LWin & 4::Run, DesktopSwitcher.exe 3, , hide
LWin & 5::Run, DesktopSwitcher.exe 4, , hide
```


AlwaysOnTop.ahk
```
#NoEnv	;
#Warn	;
SendMode Input	;
SetWorkingDir %A_ScriptDir%	;

LWin::return

LWin & F1::Winset, Alwaysontop, , A
```


RunUeli.ahk
```
#NoEnv	;
#Warn	;
SendMode Input	;
SetWorkingDir %A_ScriptDir%	;

LWin::return

LWin & R::
Send #{NumpadPgUp}
WinActivate, ahk_exe ueli.exe
```

* ueli set hotkey Super+Numpad and turn off plugins you dont need

* run shell:startup to get to startup folder and drop shorcuts 
to scrips and anything else you need to start on windows boot

* maybe run some debloater script or manualy unsitall/disable junk

* switch back to linux as soon as you can xD
