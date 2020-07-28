---
layout: post
title: "Manifest 파일에 대하여"
date: 2020-07-29
excerpt:
tags: [Android]
comments: true
---

# Manifest 파일이란?
<br> <br>
manifest의 사전적 정의는 'If you say that something is manifest, you mean that it is clearly true and that nobody
would disagree with it if they saw it or considered it.' 이다. 이를 우리말의 뉘앙스로 표현해보자면 명백하거나 분명하다는 뜻이 될 수 있다. Android Studio에서의 manifest파일은
 이러한 manifest의 사전적 정의를 따라 app에 관한 필수 정보를 '분명하게' 설명하는 파일이다.
<br> <br>
 manifest 파일에서 명시되어 있는 정보들은 다음과 같다 <br>


- 패키지의 이름에 대한 정보
- Activity, Service, BroadcastReceiver, ContentProvider와 같은 app component에 대한 정보
- 권한에 대한 정보 (사용자 데이터 또는 특정 시스템 기능에 액세스하기 위한 권환을 요청하는 부분)
- 기기 호환성에 대한 정보


<br>
 manifest 파일의 루트 요소는 app의 패키지 이름에 대한속성을 필요로 한다. 예를 들어, 패키지 이름이
"com.example.firstproject"인 경우 manifest 파일의 루트 요소는 다음과 같다. <br>


```
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.firstproject">
...
</manifest>
```
<br>
<manifest> 요소는 꼭 <application> 요소를 포함해야 한다. 구문으로 예를 들어보자.
<br>

```
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.firstproject">
<application>
...
</application>
...
</manifest>
```
이와 같이 manifest파일에는 <manifest>요소와 <application>요소가 필수적으로 '한 번' 존재해야 한다. 다른 요소들은 존재하지 않아도 되고
한 번 이상 존재해도 된다.
