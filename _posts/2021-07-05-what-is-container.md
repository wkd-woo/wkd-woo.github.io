---
layout: post
title: "컨테이너(container) 란?"
excerpt: "컨테이너의 개념"
date: 2021-07-05 20:58:30
categories:
    - Blog
tags:
    - [docker]
comments: false
---

![컨테이너](/assets/img/컨테이너.png)


> ## 🐳 *`컨테이너(Container)` 란?* 


컨테이너(Container)는 `격리된 공간` 에서 프로세스가 동작하는 기술이다.

기존의 가상화나 클라우딩 컴퓨터를 설명할 때는 VMware나 VirtualBox와 같은 Virtual Machine이 사용되었다. 

Virtual Machine은 호스트 OS위에 게스트 OS 전체를 가상화하여 사용하던 방식인데, **무겁고 느리다는 단점**이 있다.

컨테이너는 이 성능적 단점을 보다 개선한 시스템이다.


![vmAndContainer](/assets/img/vmAndContainer.png)
*<center>컨테이너와 가상 머신의 차이(https://tech.osci.kr/2020/03/03/91690167/)</center>* 
<br>

왼쪽은 가상 머신의 구조이고, 오른쪽은 컨테이너의 구조이다.
 
컨테이너에는 호스트 운영체제 위에 도커가 있고, 바로 애플리케이션이 위치한다.

반면 가상 머신은 하이퍼바이저 위에 가상 머신마다 운영체제가 있고 그 위에 애플리케이션이 위치한다.

즉, 구조 레이어가 더 간단한 컨테이너가 가상 머신보다 성능을 높이기 쉬운 것이다.

---

![docker-logo](/assets/img/docker-logo.png)
*<center> docker 로고 </center>*
<br>

컨테이너를 사용할 때, `도커`를 이용하면 간단한 명령으로 컨테이너 이미지를 만들고 저장소에 저장할 수 있다.

도커를 설치한 호스트에 해당 `컨테이너 이미지` 를 다운로드해서 컨테이너를 실행할 수 있는데,

화물 선박의 컨테이너처럼 **규격화한 컨테이너**를 만든 후 실행하려는 호스트로 옮겨서 그대로 사용하는 시스템이다.

<br>

![docker](https://docs.docker.com/engine/images/architecture.svg
)
<center>*https://docs.docker.com/get-started/overview/*</center>

<br>

컨테이너가 등장하기 전에는 호스트에도 개발 환경에 필요한 설정을 똑같이 해야 했다.

이 과정에서 여러가지 장애 요소가 동반되어 어려움이 있었는데, 

이런 불편한 점을 `컨테이너`와 `컨테이너 오케스트레이션 시스템`을 함께 사용하면서 해결할 수 있었다.

<br>

> *결과적으로 애플리케이션의 배포 및 관리가 편하고 강력해 진 것이다.*

<br>
<br>

---

###### 참고문헌 : 쿠버네티스 입문(정원천, 공용준, 홍석용, 정경록 저), 동양북스