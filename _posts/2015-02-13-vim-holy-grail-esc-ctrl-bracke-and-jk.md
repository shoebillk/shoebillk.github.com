---
layout: post
title: "Vi에서의 Esc 기원 그리고 Ctrl-[ 와 jk"
description: "Vim 에서 Esc 의 위치에 대해"
category: "vim"
tags: [vim]
---
Vim을 사용하다 보면 가끔 이런 생각이 들때가 있습니다.

> 왜 타이핑이 어려운 Esc키로 모드 전환을 했을까

Vim에서 Esc키는 삽입 모드에서 명령 모드로 전환하는 키로 아주 자주 쓰이는 키에 속합니다. 방향키를 누르기 위한 손의 움직임 조차 줄이려고 hjkl 키로 방향키를 대신할 만큼 단축키 선정에서 효율성을 중시하는 툴이 아주 자주 쓰이는 전환 키를 불편한 Esc 로 선정했다는 것은 납득이 되지 않았습니다. 

[The Vim Holy Grail](http://federico.galassi.net/2012/06/20/the-vim-holy-grail/)를 읽고 조금 이해하게 되었습니다. 요약을 하면. 

> Vi가 만들어질 당시에 쓰였던 키보드는 ADM3A 이란 터미널에 딸려 있는 키보드였다. 이 키보드를 기준으로 만든 Vi에서는 Esc키는 모드 전환에 적당한 키였다. 이후 키보드 레이아웃이 바뀌면서 Esc는 자주 누르기 불편한 위치로 이동했다.

![ADM3A keyboard layout](http://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/KB_Terminal_ADM3A.svg/931px-KB_Terminal_ADM3A.svg.png)

입니다. 
한편, 불편한 Esc 키의 위치를 극복하기 위해 Esc 키를 대체하는 전환키로 Ctrl-[ 와 jk 등의 키가 사용되기도 합니다.
