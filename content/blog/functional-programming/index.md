---
title: 함수형 프로그래밍
date: "2020-01-22"
description: "에릭 엘리엇의 소프트웨어 컴포징 언해본"
---

"Sometimes, the elegant implementation is just a function. Not a method. Not a class. Not a framework. Just a function." ~ John Carmack (Id Software, Oculus VR

추상화 프로세스에는 크게 두 가지 주된 컴포넌트가 있습니다.
  일반화는 반복되는 패턴에서 명확한 유사점을 찾고, 추상화 뒤에 유사성을 숨기는 과정입니다.
  전문화는 추상화를 사용하는 프로세스로, 각 사용사례마다 의미있는 다른 것만 제공합니다.

추상화는 개념의 기본 본질을 추출하는 프로세스 입니다.


functor 는 매핑할 수 있는 것.
예를들면 배열. [1,2,3].map(x => x * 2) // => 2,4,6
매핑할수 있는 것 이란?
  => 값들의 집합
    => 모든 값을 가져와서, 각 값에 대해 함수를 호출하고 결과를 동일한 구조와 모양의 새 컨테이너에 넣는것.
    입력 컨테이너와 출력 컨테이너의 구조가 유지되어야 함. 단, type은 변경될 수 있음.

펑터는 composition low를 준수해야함
  F.map(x => f(g(x))) 는
  F.map(g).map(f) 랑 같음

functor laws
  Identity
  Composition


Monad

// 순서가 있는 연산을 처리하는 디자인 패턴??

Map 은 a를 함수에 적용하면, b가 나오는 것. 입력이 있으면 출력하는것.

컨텍스트는 모나드 합성에 대한 계산 세부 사항