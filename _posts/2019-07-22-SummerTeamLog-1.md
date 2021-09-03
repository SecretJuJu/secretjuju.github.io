---
layout: post
title: 'TeamLog 과제 [ ip ]'
date: 2019-07-22
author: JSB
color: rgb(100,50,100)
cover: '/screenshot/TeamLog/TeamLog.png'
tags: Teamlog homework ip
---

> IP에 대해 조사 하여 IP가 무엇인지, CLASS, IPv4 대해 보고서 작성

## ip란
	ip란 internet protocol의 약자로 모든 컴퓨터(네트워크 기기)들이
    통신을 하기위해 각자의 주소(고유 식별번호)이다.
	ip를 개개인이 관리하게되면 ip가 같음등의 문제가 발생할 수 있기때문에
    각 나라별로 ip주소를 관리하는 기관이 있다.
    우리나라는 [한국인터넷진흥원] 에서 ip주소를 관리하고 있다.

	1981년 9월 ipv4가 발명되었고 이 프로토콜은 전세계적으로 사용하는
    첫번째 인터넷 프로토콜이 된다.


## ip주소의 형태
	인터넷을 하거나 학교에서 네트워크시간에 조금 이용했던 것 처럼
    많이 봐왔던 ip주소는 대충 이런식으로 생겼었다.
    192.168.0.1 <= 이런식으로
    ip주소는 4개의 옥텟으로 이루어져 있는데 옥텟이란 아래 사진과 같다.

![Octet](/screenshot/TeamLog/ip-1/ip-1.png)

	빨간색으로 밑줄쳐놓은것 하나하나가 옥텟이라 부른다.
    ip는 32비트(4바이트)로 구성되있고 한 옥텟당 8비트씩이다.
    그리고 그 옥텟들을 '.' (점)으로 구별한다.
    지금까진 봐온 ip들은 다 이진수를 십진수로 나타낸 것들이었던 것이다.
    아이피는 사실 아래와 같이생겼다.

![ip](/screenshot/TeamLog/ip-1/ip-2.png)

	8비트짜리 2진수니까 한 옥텟당 가질 수 있는 값의 갯수는 256까지 일 것이다
    0 ~ 255 까지일 테니

![range of ip](/screenshot/TeamLog/ip-1/ip-3.png)

## Network ID 와 Host ID
	네트워크상에는 수많은 ip가 있다. 이 많은 Host들을 전부 관리하는것은
    너무 힘들다. 그래서 Network ID아이디와 Host ID를 이용하여
    네트워크의 범위를 지정하여 사용한다.
    Network ID와 Host Id는 서브넷마스크를 통해 조절하게 된다.

> <a href="https://limkydev.tistory.com/166">참고 블로그</a>

## ip의 Class
	현재 ip에는 5개의 클래스가 존재한다.
    A , B , C , D , E (D 와 E는 멀티캐스트용 , 연구용 으로 사용한다고 한다...)
    위와같은 클래스들이 존재하고 이 Class들을 이용하여 ip의 Network
    host범위를 구별할 수 있다.
    A클래스는 첫번째 옥텟만 네트워크 범위이다.
    B클래스는 첫번째,두번째 옥텟만 네트워크 범위이다.
	C클래스는 첫번째,두번째,세번째 옥텟이 네트워크 범위이다.

![Class table](/screenshot/TeamLog/ip-1/ip-4.png)

<hr/>

> 위 표는 이 <a href="https://limkydev.tistory.com/168">블로그를 참고하였다.</a>

	A 클래스는 0으로 시작한다.
    B 클래스는 10으로 시작한다.
    C 클래스는 110으로 시작한다.

<table class="txc-table" width="784" cellspacing="0" cellpadding="0" border="0" style="border:none;border-collapse:collapse;;font-family:Dotum, 돋움;font-size:16px"><tbody><tr><td style="width: 75px; height: 24px; border-width: 1px; border-style: solid; border-color: rgb(204, 204, 204);"><p>&nbsp;클래스&nbsp;</p></td>
<td style="width: 111px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-top: 1px solid rgb(204, 204, 204);"><p>&nbsp;첫째 옥텟 IP</p></td>
<td style="width: 61px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-top: 1px solid rgb(204, 204, 204);"><p style="text-align: center;">최상위&nbsp;</p><p style="text-align: center;">비트</p></td>
<td style="width: 270px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-top: 1px solid rgb(204, 204, 204);"><p>&nbsp;범위</p></td>
<td style="width: 98px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-top: 1px solid rgb(204, 204, 204);"><p>&nbsp;호스트 수</p></td>
<td style="width: 102px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-top: 1px solid rgb(204, 204, 204);"><p>&nbsp;네트워크&nbsp;수</p></td><td style="width: 64px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-top: 1px solid rgb(204, 204, 204);" colspan="1">&nbsp;블록</td>
</tr>
<tr><td style="width: 75px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-left: 1px solid rgb(204, 204, 204);"><p>&nbsp;Class A</p></td>
<td style="width: 111px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;0&nbsp;~ 126</p></td>
<td style="width: 61px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;0</p></td>
<td style="width: 270px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;0.0.0.0 ~ 127.0.0.0</p></td>
<td style="width: 98px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);">&nbsp;16,777,216</td>
<td style="width: 102px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);">&nbsp;128</td><td style="width: 64px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="1">&nbsp;/8</td>
</tr>
<tr><td style="width: 75px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-left: 1px solid rgb(204, 204, 204);"><p>&nbsp;Class B</p></td>
<td style="width: 111px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;128 ~ 191</p></td>
<td style="width: 61px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;1</p></td>
<td style="width: 270px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;128.0.0.0 ~ 191.255.0.0</p></td>
<td style="width: 98px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);">&nbsp;65,536</td>
<td style="width: 102px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;16,384</p></td><td style="width: 64px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="1">&nbsp;/16</td>
</tr>
<tr><td style="width: 75px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-left: 1px solid rgb(204, 204, 204);"><p>&nbsp;Class C</p></td>
<td style="width: 111px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;192 ~ 223</p></td>
<td style="width: 61px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;11</p></td>
<td style="width: 270px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;192.0.0.0 ~ 223.255.255.0</p></td>
<td style="width: 98px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);">&nbsp;256</td>
<td style="width: 102px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);">&nbsp;2,097,152</td><td style="width: 64px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="1"><p>&nbsp;/24</p></td>
</tr>
<tr><td style="width: 75px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-left: 1px solid rgb(204, 204, 204);"><p>&nbsp;Class D</p></td>
<td style="width: 111px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;224 ~ 239</p></td>
<td style="width: 61px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;111</p></td>
<td style="width: 270px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;224.0.0.0 ~ 239.255.255.255</p></td>
<td style="width: 198px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="2" rowspan="1"><p>&nbsp;N/A(268,435,456)</p></td><td style="width: 64px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="1" rowspan="1"><p>&nbsp;N/A</p></td>

</tr>
<tr><td style="width: 75px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204); border-left: 1px solid rgb(204, 204, 204);"><p>&nbsp;Class E</p></td>
<td style="width: 111px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;240 ~ 255</p></td>
<td style="width: 61px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;1111</p></td>
<td style="width: 270px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);"><p>&nbsp;240.0.0.0 ~ 247.255.255.255</p></td>
<td style="width: 198px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="2" rowspan="1">&nbsp;N/A(268,435,456)</td><td style="width: 64px; height: 24px; border-bottom: 1px solid rgb(204, 204, 204); border-right: 1px solid rgb(204, 204, 204);" colspan="1" rowspan="1">&nbsp;N/A</td>

</tr>
</tbody></table>

<hr/>

> 위 테이블은 <a href="https://raisonde.tistory.com/entry/IP%EC%A3%BC%EC%86%8C-ABC%ED%81%B4%EB%9E%98%EC%8A%A4-%EB%B0%8F-%EC%84%9C%EB%B8%8C%EB%84%B7%EC%97%90-%EB%8C%80%ED%95%9C-%EC%9D%B4%ED%95%B4"> 이 블로그</a>에서 참고하였다.

### TIP
	약간 여태껏 많이 궁금했던건데 과제는 아니지만 소소한 tip을 준비했다.
    php를 실습할때 127.0.0.1 로 접속하여 내가 만든 php파일이 잘 돌아가는지
    확인하거나 192.168.0.1 등으로 게이트웨이를 설정하거나 할때 왜 하필
    이 번호를 쓰는지 궁금했었는데 과제를 하려 자료를찾다가 발견해버렸다.

<table class="txc-table" width="964" cellspacing="0" cellpadding="0" border="0" style="border:none;border-collapse:collapse;;font-family:돋움;font-size:12px"><tbody><tr><td style="width: 482px; height: 24px; border: 1px solid rgb(124, 132, 239); background-color: rgb(242, 203, 97);"><p style="text-align: center;"><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-align: center; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">주소 대역</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-top-width: 1px; border-top-style: solid; border-top-color: rgb(124, 132, 239); background-color: rgb(242, 203, 97);"><p style="text-align: center;"><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-align: center; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">용도</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">0.0.0.0/8</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">자체 네트워크</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">10.0.0.0/8</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">사설 네트워크</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">127.0.0.0/8</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="text-indent: -36.47999954223633px; color: black; font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">루프백</span><span style="text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; color: black; font-size: 10pt; background-color: transparent;">(loopback)&nbsp;</span><span style="text-indent: -36.47999954223633px; color: black; font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">즉</span><span style="text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; color: black; font-size: 10pt; background-color: transparent;">,&nbsp;</span><span style="text-indent: -36.47999954223633px; color: black; font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">자기자신</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">169.254.0.0/16</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="text-indent: -36.47999954223633px; color: black; font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">링크 로컬</span><span style="text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; color: black; font-size: 10pt; background-color: transparent;">(</span><span style="text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; color: black; font-size: 10pt; background-color: transparent;">link local)</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">172.16.0.0/12</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">사설 네트워크</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">192.0.2.0/24</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">예제 등 문서에서 사용</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">192.88.99.0/24</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; color: black; font-size: 10pt; background-color: transparent;">6to4&nbsp;</span><span style="text-indent: -36.47999954223633px; color: black; font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">릴레이&nbsp;</span><span style="text-indent: -36.47999954223633px; color: black; font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">애니캐스트</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">192.168.0.0/16</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">사설 네트워크</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">198.18.0.0/15</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">네트워크 장비 벤치마킹 테스트</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; background-color: transparent;">224.0.0.0/4</span></p></td>
<td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);"><p><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif; background-color: transparent;">멀티캐스트</span></p></td>
</tr>
<tr><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(124, 132, 239);" rowspan="1"><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-family: Gulim, 굴림, AppleGothic, sans-serif; font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px;">240.0.0.0/4</span></td><td style="width: 482px; height: 24px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(124, 132, 239); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(124, 132, 239);" rowspan="1"><span style="font-size: 10pt; font-family: Gulim, 굴림, AppleGothic, sans-serif;">&nbsp;</span><span style="color: rgb(0, 0, 0); font-size: 10pt; line-height: 24px; text-indent: -36.47999954223633px; font-family: Gulim, 굴림, AppleGothic, sans-serif;">미래 사용 용도로 예약</span></td></tr></tbody></table>

출처 : <a href="https://nitw.tistory.com/22">https://nitw.tistory.com/22</a>