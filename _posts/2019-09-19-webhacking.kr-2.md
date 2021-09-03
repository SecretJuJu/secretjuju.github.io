---
layout: post
title: 'WebHacking.kr_32'
date: 2019-09-19
author: JSB
color: rgb(100,50,100)
cover: '/screenshot/WebHacking/webhacking.kr.jpg'
tags: wargame.kr webhacking
---

> 공부한것을 쓰려했지만 아직 공부중인 것을 끝내지못해 문제풀이로 대체한다!

# WebHacking.kr 32번

<img src="/screenshot/WebHacking/3/1.png">

	문제에 들어가면 다음과 같은 화면에 닉네임을 누르면 투표를 할 수있게 되어있다.
    이 투표수를 1위로 찍으면 풀리는 문제인 것 같다.

<img src="/screenshot/WebHacking/3/2.png">

	2번이상 투표를 하려하면 이미 투표가 끝났다고 한다.
    하지만 내가 투표를 했는지 안했는지 확인하는 것을 발견하여
    변경할 수 있다면 이 투표를 조작할 수 있을지도 모른다.

<img src="/screenshot/WebHacking/3/3.png">

	빙고!
    vote_check 라는 쿠키가 이름부터 나의 투표를 막을 것 같이 생겼다.
    하지만 이 값을 지우고 투표하고 지우고 클릭하고하면 어느세월에 1위를 찍겠는가...
    그래서 이걸 자동으로 해주는 파이썬코드를 짰다.

<div class="colorscripter-code" style="color:#010101;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#fafafa;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #e5e5e5"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#666;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div><div style="line-height:130%">5</div><div style="line-height:130%">6</div><div style="line-height:130%">7</div><div style="line-height:130%">8</div><div style="line-height:130%">9</div><div style="line-height:130%">10</div><div style="line-height:130%">11</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#010101;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#a71d5d">import</span>&nbsp;requests</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">url&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;<span style="color:#63a35c">'https://webhacking.kr/challenge/code-5/'</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">cookie&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;{</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#63a35c">'PHPSESSID'</span>:<span style="color:#63a35c">'754mv31u9mtbiq3t90g47617r4'</span>,&nbsp;<span style="color:#999999">#&nbsp;&lt;=&nbsp;자신의&nbsp;or&nbsp;아무&nbsp;세션값</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#63a35c">'vote_check'</span>:<span style="color:#63a35c">'&nbsp;'</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">}</div><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#a71d5d">for</span>&nbsp;i&nbsp;<span style="color:#a71d5d">in</span>&nbsp;<span style="color:#066de2">range</span>(<span style="color:#0099cc">0</span>,<span style="color:#0099cc">13</span>):</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;param&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;{<span style="color:#63a35c">'hit'</span>:<span style="color:#63a35c">'자신의&nbsp;아이디'</span>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#999999">#&nbsp;&lt;=&nbsp;자신의&nbsp;닉네임</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;requests.get(url,params<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>param,cookies<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>cookie)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#066de2">print</span>(<span style="color:#63a35c">"vote&nbsp;complete"</span>)</div></div><div style="text-align:right;margin-top:-13px;margin-right:5px;font-size:9px;font-style:italic"><a href="http://colorscripter.com/info#e" target="_blank" style="color:#e5e5e5text-decoration:none">Colored by Color Scripter</a></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none;color:white"><span style="font-size:9px;word-break:normal;background-color:#e5e5e5;color:white;border-radius:10px;padding:1px">cs</span></a></td></tr></table></div>

	for문의 range 함수의 2번째 인자에 올릴만큼의 투표수를 넣으면 된다.