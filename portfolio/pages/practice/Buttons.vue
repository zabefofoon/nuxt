<template>
  <div>
    <v-container>
      <h1 class="headline font-weight-bold">Buttons and Icons</h1>
      <p class="body-1">Vuetify에서 제공하는 버튼과 아이콘을 사용해보자.</p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Buttons</h2>
      <p class="body-1">상황에 따라서 잘 사용해보자.</p>
      <div class="code-box">
        <v-btn>Button</v-btn><br /><br />
        <v-btn elevation="2" disabled>Disabled</v-btn><br /><br />
        <v-btn loading>Loading</v-btn><br /><br />
        <v-btn color="red" class="white--text">Color</v-btn><br /><br />
        <v-btn rounded>Rounded</v-btn><br /><br />
        <v-btn fab>FAB</v-btn><br /><br />
        <v-btn><v-icon left>mdi-arrow-down</v-icon> Icons</v-btn><br /><br />
        <v-btn block>Block</v-btn>
      </div>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">Icons</h2>
      <p class="body-1">
        "https://materialdesignicons.com/"에서 잘 찾아보자.<br />
        "mdi-" 접두사를 붙이자.
      </p>
      <div class="code-box">
        <v-icon>mdi-arrow-down</v-icon>
        <v-icon>mdi-camera-outline</v-icon>
        <v-icon color="green">mdi-domain</v-icon>
      </div>
    </v-container>
  </div>
</template>
