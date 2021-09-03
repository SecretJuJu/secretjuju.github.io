---
layout: post
title: 'ADAP , tunnel'
date: 2019-08-26
author: JSB
color: rgb(100,50,100)
cover: '/screenshot/HelloWorld.png'
tags: Introduce Network tunnel
---

# ADAP
	선린인터넷고 1학년 3반 연규와 선우가 만든
    하루에 1개씩 블로그를 써야하는 동아리이다.

## 내가 올리게될 블로그의 CATEGORY:

1. 웹해킹
2. 네트워크
3. mics
	꼭 웹해킹과 네트워크가 아니더라도 다른 잡다한 것 들도 올릴 예정이다.

* 지금까지 블로그 쓰면서 느낀건데 블로그의 말투를 ~요 / ~다
	이 둘중 어느것을 골라야할지 고민하다가 그냥 편한 ~다. 이런 말투로 진행하게 될 것이다.

# Tunnel
	터널.. 회사에서 본사와 지사를 연결할때 만약 따로 회선을 만든다면
    비용이 얼마나 들까.? 본사와 지사를 다이렉트로 연결하고 싶지만
    비용이 너무 많이들기에 ISP를 거쳐가게 되어있다.
    하지만 ISP를 거쳐가면서 논리적으로 다이렉트로 연결할 방법이 있을까?
    바로 Tunnel을 뚫는것이다. 
    
<img src="/screenshot/network/Tunnel/1.png">


여기서 나는 왼쪽라우터와 오른쪽라우터를 논리적으로 바로 연결하고 싶다.
원래대로 통신을 하면

<img src="/screenshot/network/Tunnel/2.png">

다음과 같이 중간에 ISP를 거친것으로 표시가 된다. 하지만 여기에 터널을 설정하면

왼쪽
interface Tunnel10
 ip address 1.1.1.1 255.255.255.252
 mtu 1476
 tunnel source Serial0/0/0
 tunnel destination 10.0.0.6
ip route 192.168.20.0 255.255.255.0 1.1.1.2 

오른쪽 라우터

interface Tunnel10
 ip address 1.1.1.2 255.255.255.252
 mtu 1476
 tunnel source Serial0/0/0
 tunnel destination 10.0.0.1
ip route 192.168.10.0 255.255.255.0 1.1.1.1 

<img src="/screenshot/network/Tunnel/3.png">

위처럼 터널을 거쳐갔다고 표시된다. 하지만 실제로 wireshark등으로 해당 패킷을 잡게되면
GRE라는 패킷이 붙어있는것을 볼 수 있다.

보통 이 터널에서 GRE라는 프로토콜을 이용해 IPSEC을 이용해 VPN을 구성하게 된다.

뭔가 인사만하고 끝내기 아쉬워서 최소한의 양심으로 네트워크에 관한 이야기좀 해 보았다.