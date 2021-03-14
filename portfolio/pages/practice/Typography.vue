<template>
  <div>
    <v-container>
      <h1 class="headline font-weight-bold">Typography</h1>
      <p class="body-1">Vuetify에서 제공하는 class로 글자를 꾸며보자.</p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">제목</h2>
      <p class="body-1">
        한글로는 제목, 표제 등으로 이야기 하지만, 영어에서는 이를 표시하는데,
        "headline", "title", "subtitle" 등으로 이야기하며, <br />
        광고 쪽에서는 이와 같은 역할을 하는 것을 "헤드카피", "서브카피",
        "리드카피", "바디카피" 라고 한다.<br /><br />
        Vuetify에서는 ".display-(1~4)", ".headline", ".title",
        ".subtitle-(1~2)", ".subheading", "text-{breakPoint}-{h1~h6}"이 있다.
      </p>
      <div class="code-box">
        <h1 class="text-h1">.text-h1</h1>
        <h2 class="text-h2">.text-h2</h2>
        <h3 class="display-3">.display-3</h3>
        <h3 class="display-2">.display-2</h3>
        <h3 class="display-1">.display-1</h3>
        <h3 class="headline">.headline</h3>
        <h3 class="title">.title</h3>
        <h3 class="subtitle-1">.subtitle-1</h3>
        <h3 class="subtitle-2">.subtitle-2</h3>
        <h3 class="subheading">.subheading</h3>
      </div>
      <p class="body-1">
        역할에 따라 class를 부여하는게 좋을지, 생긴것에 따라 class를 부여하는게
        좋을지 모르겠지만,<br />개인적으로는
        생긴것("text-{breakPoint}-{h1~6}")를 사용하는게 좋을 것 같다.
      </p>
      <p class="caption">
        https://m.blog.naver.com/grubiz/221653000018<br />
        https://www.italki.com/post/discussion-88735?hl=en<br />
        https://terms.naver.com/entry.nhn?docId=17833&cid=43659&categoryId=43659<br />
        https://vuetifyjs.com/en/styles/text-and-typography/#typography
      </p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">본문과 그 외</h2>
      <p class="body-1">
        본문으로는 ".body-1", ".body-2", 설명문으로는 ".overline", 캡션으로는
        ".caption"을 사용하자.
      </p>
      <div class="code-box">
        <p class="body-1">.body-1 본문1</p>
        <p class="body-2">.body-2 본문2</p>
        <p class="overline">.overline 설명문</p>
        <p class="caption">.caption 캡션</p>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Font-weight 와 Italic</h2>
      <p class="body-1">
        폰트 굵기로는 ".font-weight-black", ".font-weight-bold",
        ".font-weight-medium", ".font-weight-regular", ".font-weight-light",
        ".font-weight-thin",<br />
        이탤릭으로는 ".font-italic" 사용하자.
      </p>
      <div class="code-box">
        <p class="font-weight-black">.font-weight-black</p>
        <p class="font-weight-bold">.font-weight-bold</p>
        <p class="font-weight-medium">.font-weight-medium</p>
        <p class="font-weight-regular">.font-weight-regular</p>
        <p class="font-weight-light">.font-weight-light</p>
        <p class="font-weight-thin">.font-weight-thin</p>
        <p class="font-italic">.font-italic</p>
      </div>
      <p class="body-1">
        thin은 상황에 따라 폰트가 깨져보이므로 사용하지 말아야겠다.
      </p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">정렬</h2>
      <p class="body-1">
        양끝 정렬은 ".text-justify", 좌우 정렬은
        ".text-{breakpoint}-{direction}"을 사용하자.
      </p>
      <div class="code-box">
        <p class="text-justify">
          .text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify.text-justify
        </p>
        <p class="text-center">.text-center</p>
        <p class="text-right">.text-right</p>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">장식</h2>
      <p class="body-1">
        ".text-decoration-overline", ".text-decoration-underline",
        ".text-decoration-through"
      </p>
      <div class="code-box">
        <p class="text-decoration-overline">.text-decoration-overline</p>
        <p class="text-decoration-underline">.text-decoration-underline</p>
        <p class="text-decoration-line-through">.text-decoration-through</p>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">투명도 그 외</h2>
      <p class="body-1">
        투명도는 ".text--primary", ".text--secondary", ".text--disabled"<br />
        말줄임은 ".text-truncate"를 사용하자.
      </p>
      <div class="code-box">
        <p class="text--primary">.text--primary</p>
        <p class="text--secondary">.text--secondary</p>
        <p class="text--disabled">.text--disabled</p>
        <p class="text-truncate" style="max-width:100px;">
          .text-truncate .text-truncate
        </p>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">색상</h2>
      <p class="body-1">
        배경은 ".red", 글자 색은 ".red--text"를 사용하자.
      </p>
      <div class="code-box">
        <p class="orange">.orange</p>
        <p class="orange--text">.orange--text</p>
      </div>
    </v-container>
  </div>
</template>
