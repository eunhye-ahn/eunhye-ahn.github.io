---
title:  "Collection"
categories: java
tag: [java]
toc: true
author_profile: false
published: true
sidebar:
    nav: "docs"
--- 

컬렉션 프레임워크란 많은 데이터를 처리하기위해 자바가 제공해주는 클래스의 집합이다.

컬렉션 프레임워크에는 대표적으로 List, Set, Map 이 있다.

# ArrayList
일반적으로 int[] array = new int[3]; 으로 배열의 크기를 지정하기 때문에 데이터의 삽입과 삭제가 어렵다. 하지만 List를 사용하면 배열의 크기를 따로 지정하지 않기 때문에 데이터의 삽입과 삭제가 쉬워 많은 양의 데이터를 처리하기 보다 쉽다.

```java
ArrayList<자료형> 리스트명 = new ArrayList<>();

// 데이터 추가
list.add("고양이");
list.add("강아지");
list.add("사자");
list.add("악어");
list.add("호랑이");


// 데이터 조회(인덱스)
list.get(0);
list.get(1);
list.get(2); 

// 데이터 삭제
list.remove(0)
list.remove("강아지")

// 마지막 인덱스 삭제
list.remove(list.sizeof()-1)

// 데이터 순회
for (String s : list) {
    System.out.println(s);
}

// 데이터 변경
list.set(0,"호랑이");

// 데이터 확인(인덱스 위치 검색)
list.indexof("사자");

// 리스트 내 포함여부 확인
list.contains("악어");

// 데이터 전체 삭제
list.clear();
if(list.isEmpty()){
    System.out.println("데이터 전체 삭제 확인");
}

// 데이터 정렬
Collections.sort(list);
```
# LinkedList
링크 리스트는 어레이 리스트와 대체적으로 비슷하다.
하지만 어레이 리스트와 달리 링크 리스트는 데이터를 삽입할 때 특정 위치로 삽입하는 addFirst(), addLast() 메서드를 추가적으로 사용할 수 있다. 
```java
LinkedList<String> list = new LinkedList<>();

list.add("강아지")
list.addFirst("고양이");
list.addLast("토끼");
```
데이터 삭제도 마찬가지로 remove로도 가능하지만, removeFirst(),removeLast() 메서드를 사용할 수 있다.

그 외는 어레이리스트와 동일하다.