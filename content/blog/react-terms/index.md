---
title: react terms
date: "2020-02-07T22:17:00.000Z"
description: "react terms list simple description"
---

# windowing
페이지 전체 렌더링 대신, 현재 보고 있는(스크롤이 위치한) 부분만 렌더링 하는 기법입니다.

다음과 같은 라이브러리가 있습니다.
<a href="https://react-window.now.sh/#/examples/list/fixed-size" target="_blank">react-window</a>  
<a href="https://bvaughn.github.io/react-virtualized/#/components/List" target="_blank">react-virtualized</a>  

# Reconciliation
VDOM diff
화면에 변화가 있을 때만 렌더링을 합니다.

## diffing algorithm
먼저 엘리먼트의 타입을 비교합니다. 타입이 다르면 해당 엘리먼트를 재구축합니다. 타입이 같으면 각 attribute를 비교하여, 변경된 attribute만 갱신합니다.
이 작업은 재귀적으로 이루어집니다.

## diffing cost
node의 수가 아니라, view의 크기에 비례합니다.
```html
<WrapNode>
	<div></div>
	<div>{state}</div>
	<div></div>
</WrapNode>
```
state가 변경되면, WrapNode가 변경됩니다.

자세한 설명은 <a href="https://ko.reactjs.org/docs/reconciliation.html">리액트 홈페이지</a>를 참조하세요.

## Perceived Performance
인지적 성능개선.
Time Slicing
Scheduling [Prioritization, Concurrency]