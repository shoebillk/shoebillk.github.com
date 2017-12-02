---
layout: post
category : mongodb 
tagline: ""
tags : [lldb]
title: "lldb fr v 로 hexa 값 출력하기"
---
lldb 의 fr v 명령어는 해당 프레임에 변수를 출력하는 명령어입니다. 이 명령어의 출력은 기본이 10 진수로 표현되는데 16진수나 2진수로 출력하고 싶다면 아래와 같은 옵션으로 형식(hex, bin)을 정해 줍니다.

{% highlight bash %}
(lldb) fr v flag
(int) flag = 546
{% endhighlight %}

{% highlight bash %}
(lldb) fr v flag -f hex
(int) flag = 0x00000222
(lldb) fr v flag -f bin
(int) flag = 0b00000000000000000000001000100010
{% endhighlight %}
