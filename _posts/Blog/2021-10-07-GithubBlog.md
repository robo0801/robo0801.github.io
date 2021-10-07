---
layout: single


title: "[Github Blog] Blog Create"

toc: true
toc_label: "My Table of Contents"


categories:
  - GithubBlog

---

# Github blog 만들기!

### Blog 생성 및 설정
[테디노트Youtube](https://www.youtube.com/watch?v=ACzFIAOsfpM&t=395s)

[oilmlio world](https://oilmlio.com/blog/How-to-Create-a-GitHub-Blog/#1-%EC%83%88%EB%A1%9C%EC%9A%B4-%EB%B8%94%EB%A1%9C%EA%B7%B8%EB%A5%BC-%EC%8B%9C%EC%9E%91%ED%95%98%EB%8B%A4)

#### Themes 추천 
[Yet Another Theme](http://jekyllthemes.org/themes/jekyll-theme-yat/)


### config.yml 수정
[7271kim github blog](https://github.com/7271kim/7271kim.github.com/blob/master/_config.yml)



# Github Blog fontsize 변경
Blog font size가 너무 커서 가독성이...  
변경 방법!  


### _reset.scss 수정

/_sass/minimal-mistakes/_reset.scss 에서 html 부분을 수정한다.  

```css  
html {
  /* apply a natural box layout model to all elements */
  box-sizing: border-box;
  background-color: $background-color;
  font-size: 14px;
  @include breakpoint($medium) {
    font-size: 14px;
  }
  @include breakpoint($large) {
    font-size: 16px;
  }
  @include breakpoint($x-large) {
    font-size: 18px;
  }
  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
}
```
## 참고
[Minimal Mistakes start guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
## 다음 할 일
[oilmlio world 파일 최적화](https://oilmlio.com/blog/minimal-mistakes-Remove-the-Unnecessary/)
https://jinhoooooou.github.io/making-blog/making-blog-7/
https://ansohxxn.github.io/blog/markdown/
대문 만들기
http://jekyllrb-ko.github.io/docs/permalinks/
https://seungwubaek.github.io/blog/home_layout/#indexhtml
## test
