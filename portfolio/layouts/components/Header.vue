<template>
  <v-app-bar app color="white" elevation="1">
    <v-container>
      <v-row>
        <v-btn text nuxt to="/" color="white" :ripple="false">
          <span class="font-weight-bold headline black--text">
            {{ title }}
          </span>
        </v-btn>
        <v-spacer />
        <v-btn
          v-for="(item, index) in items"
          :key="index"
          nuxt
          :to="item.to"
          text
          elevation="0"
          color="white"
          :ripple="false"
        >
          <span class="black--text">
            {{ item.title }}
          </span>
        </v-btn>
      </v-row>
    </v-container>
  </v-app-bar>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      title: "Saang",
      items: [
        {
          title: "Practice",
          to: "/practice",
          component: "practice/index.vue"
        },
        {
          title: "Menu",
          to: "/"
        },
        {
          title: "Menu",
          to: "/"
        }
      ]
    };
  }
};
</script>
