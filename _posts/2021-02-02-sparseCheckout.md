---
layout: post
title: "(Git) 특정 폴더만 따로 clone 하는 법"
date: 2021-02-02
excerpt: ""
tags: [Git]
comments: true
---

Git을 사용하다 보면, 특정 폴더만을 clone하고 싶은 경우(ex: 전체 폴더를 clone하기엔 부담스러운 용량일 때)가 있다. 그럴 때 사용할 수 있는 방법이 sparseCheckout 이라는 기능을 이용하는 방법이다.

---

<br>
## sparseCheckout

1. clone 받을 local repositery를 생성해준다.

<br>

~~~
mkdir cloneTest
cd cloneTest
git init Test
cd Test
~~~

<br>

2. sparseCheckout 기능을 활성화 시켜 준다.

<br>

~~~
git config core.sparseCheckout true
~~~

<br>

3. clone받고 싶은 저장소 remote를 추가해준다.

<br>

~~~
git remote add -f origin <REMOTE_URL>
~~~

<br>

4. sparseCheckout하기 원하는 파일이나 폴더를 .git/info/sparse-checkout 파일에 기술해준다.

~~~
echo "models/" >> .git/info/sparse-checkout
~~~

5. 이제 pull하면 sparse-checkout에 기술한 경로의 파일이나 폴더만 가져온다.

<br>

~~~
git pull origin master
~~~
