---
layout: post
title: "(Android) Payco의 Layout 따라해보기"
date: 2020-07-29
excerpt: ""
tags: [Android]
comments: true
---

# Payco 따라해보기
<br>
![paycoLayout](https://raw.githubusercontent.com/EastHShin/EastHShin.github.io/master/img/paycoLayout.png)
<br>
먼저, 크게 윤곽을 잡기위해 LinearLayout으로 6개의 구간을 나누었다. 첫번째 구간에서는 메뉴버튼과 페이코 로고 버튼의 위치를 배정하기 위해 constraintlayout을 사용했는데, constraintlayout을 사용하면 화면 크기의 변화에도 적절한 비율로 위치를 잡아줄수 있을거라 생각했기 때문이다. 두번째와 세번째 linearlayout구간에서도 마찬가지로 constraintlayout을 사용했다. 네번째 구간은 세번째와 다섯번째 구간의 간격을 띄우기 위한 용도로 사용하였다. 다섯번째 구간은 TableLayout을 사용해 다시 4구간으로 나누었다. 각 행에 다시 constraintlayout을 적용하여 이미지버튼들을 비율에 맞게 배치시켜주었다. 마지막으로 여섯번째 구간도 constraintlayout을 적용시켜 배치하였다.
