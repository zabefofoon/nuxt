<template>
  <div>
    <v-container>
      <h1 class="headline font-weight-bold">Layout, Flex</h1>
      <p class="body-1">v-layout과 flex에 대해 알아보자.</p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Break Point와 Flex Layout</h2>
      <p class="body-1">
        - Break Point<br/>
        "xs" = Extra small = < 600px = 핸드폰 세로<br/>
        "sm" = Small = 600px > && 960px = 핸드폰 가로, 중간정도 태블릿<br/>
        "md" = Medium = 960px > && 1264px = 큰 태블릿, 노트북<br/>
        "lg" = Large = 1264px > && 1904px = 데스크탑<br/>
        "xl" = Extra Large = 1904px > = 4K 이상 모니터, 와이드 모니터
      </p>
      <p class="body-1">
        - Flex Layout<br/>
        해당 영역을 12칸으로 나누고 컨텐츠를 칸수에 맞게 나열
      </p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Mobile First</h2>
      <p class="body-1">
        Mobile 수요가 더 많으니, "xs"부터 작성을 하자.<br/>
        "xs", "md", "lg"를 주로 쓸것 같다.
      </p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">v-flex</h2>
      <p class="body-1">
        컨텐츠를 중앙 및 수평으로 채우는 기능.<br/>
        v-container > v-layout > v-flex 순으로 테이블 레이아웃을 짤 수 있다.<br/>
        <em>이게 더 편한듯 싶다.</em>
      </p>
      <div class="code-box">
        <v-container class="border">
          <v-layout class="border">
            <v-flex class="border">v-flex</v-flex>
            <v-flex class="border">v-flex</v-flex>
          </v-layout>
          <br/>
          <v-layout class="border">
            <v-flex class="border" md8>v-flex md8</v-flex>
            <v-flex class="border" md2>v-flex md2</v-flex>
          </v-layout>
          <br/>
          <v-layout class="border" justify-space-between>
            <v-flex class="border" md4>v-flex md8<br/>justify-space-between</v-flex>
            <v-flex class="border" md4>v-flex md2<br/>justify-space-between</v-flex>
          </v-layout>
          <br/>
          <v-layout class="border">
            <v-flex class="border">v-flex</v-flex>
            <v-flex>
              <v-layout>
                <v-flex class="border" md6>v-flex</v-flex>
                <v-flex class="border" md6>v-flex</v-flex>
              </v-layout>
              <v-layout>
                <v-flex class="border" md8>v-flex</v-flex>
                <v-flex class="border" md4>v-flex</v-flex>
              </v-layout>
              <v-layout>
                <v-flex class="border" md4>v-flex</v-flex>
                <v-flex class="border" md8>v-flex</v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-container>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">v-col</h2>
      <p class="body-1">
        컨텐츠를 중앙 및 수평으로 채우는 기능.<br/>
        v-container > v-row > v-col 순으로 사용하여 그리드를 짤 수 있다.
      </p>
      <div class="code-box">
        <v-container class="border">
          <v-row class="border">
            <v-col class="border" md="8" sm="8" lg="8">v-col 8</v-col>
            <v-col class="border">v-col</v-col>
          </v-row>
        </v-container>
      </div>
    </v-container>
  </div>
</template>
