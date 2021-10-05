---
title: "[Markdown] Markdown Tutorial"

toc: true
toc_label: "Table of Contents"


categories:
  - GithubBlog

---


마크다운(markdown) 작성법
=========================

# 1 헤더 (headers)
* 큰제목: 문서제목
	```
	This is an H1
	=============
	```
	This is an H1
	=============
* 작은 제목: 문서 부제목
	```
	This is an H2
	-------------
	```
	This is an H2
	-------------
* 글머리: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6

# 2 BlockQuote
```>``` 사용한다.
```
> This is a first blockqute.
>       > This is a second blockqute.
>       >       > This is a third blockqute.
```
> This is a first blockqute.
>       > This is a second blockqute.
>       >       > This is a third blockqute.

# 3 목록
순서 목록: 숫자뒤에 점 사용
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째          .
2. 두번째
3. 세번째

순서없는 목록: 글머리 기호 사용
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑


# 4 코드
```<pre><code>내용</code></pre>```
<pre><code>내용</code></pre>


```
This is a normal paragraph:

    This is a code block.
end code block.
```
실제로 적용해보면,
This is a normal paragraph:

    This is a code block.
end code block.

# 5 수평선
아래 줄은 모두 수평선을 만든다.
```
* * *

***

*****

- - -

---------------------------------------
```

# 6 링크
* 참조링크

```
[link keyword][id]
[id]: URL "Optional Title here"

Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"

* 인라인 링크
```
syntax: [Title](link)
```
Link: [Google](https://google.com, "google link")

* 자동연결
```
<http://example.com/>
<address@example.com>
```

<http://example.com/>
<address@example.com>

# 7 강조

```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
++underline++
~~cancelline~~
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
++underline++
~~cancelline~~

# 8 이미지

```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```
![석촌호수 러버덕](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0)
![석촌호수 러버덕](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0 "RubberDuck")

사이즈 조절 기능은 없기 때문에 ```<img width="" height=""></img>```를 이용한다.


# 출처
* <https://gist.github.com/ihoneymon/652be052a0727ad59601>
