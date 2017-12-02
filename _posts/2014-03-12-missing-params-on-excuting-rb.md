---
layout: post
title: "rb 파일만 실행 시 파라미터가 넘어가지 않을 때"
description: ""
category: ""
tags: [ruby]
---

Windows에서 Ruby 파일에 파라미터를 넘겨서 아래와 같이 실행할 때,

    ruby.exe test.rb parameter

위와 같이 ruby.exe 와 함께 실행 할때는 파라미터를 잘 받아 오는데 아래와 같이 rb 파일만 실행할 때는 파라미터를 받아 오지 못하는 경우가 있습니다.

    test.rb parameter

.rb 파일과 ruby.exe와 연결되는 설정에 파라미터를 넘기는 부분이 빠져 있어 발생하는 문제입니다. 

검색을 해보면 assoc 와 ftype을 이용해서 설정을 점검하는 방법이 있습니다.

[Ruby’s ARGV is empty when run on windows](http://samuelanthony12.wordpress.com/2013/09/19/rubys-argv-is-empty-when-run-on-windows/)

그런데 이렇게 설정을 했는데도 여전히 문제가 해결되지 않았다면 레지스트리에 설정을 확인해야 합니다.

    HKEY_CURRENT_USER\Software\Classes\Applications\ruby.exe\shell\open\command
    (기본값) REG_SZ : "C:\Ruby193\bin\ruby.exe" "%1"
    
위와 같이 설정되어 있다면 아래와 같이 끝에 %* 를 추가해 주면 해결됩니다.

    (기본값) REG_SZ : "C:\Ruby193\bin\ruby.exe" "%1" %*
    


