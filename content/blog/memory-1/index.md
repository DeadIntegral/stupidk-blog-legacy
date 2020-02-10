---
title: 메모리에 대하여 알아야 할 것 Part.1
date: "2020-02-10T00:00:00.000Z"
description: "What every programmer should know about memory, Part 1 번역"
---

# 1. Intro
초창기에는 컴퓨터가 훨씬 간단했습니다. CPU, Memory, mass storage, network interface 와 같은 시스템의 구성 요소들이 함께 개발되었고, 결과적으로 성능의 규현이 잘 잡혔습니다. 예를들어, Memory 와 Network Interface는 데이터를 제공할 때 CPU보다 (훨씬) 빠르지 않았습니다.

이러한 상황은 컴퓨터의 기본 구조가 안정화되고, 하드웨어 개발자가 개별 하위 시스템 최적화에 집중 한 후 변경되었습니다. 갑자기 컴퓨터의 일부 구성 요소의 성능이 크게 저하되고 병목 현상이 발생했습니다. 이는 비용 측면에서 다른 구성 요소에 비해 느리게 개선 된 대용량 저장소 및 메모리 하위 시스템의 경우 특히 도드라졌습니다.