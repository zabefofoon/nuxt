<template>
  <v-app id="inspire">
    <Header />
    <v-main>
      <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet class="fixed" elevation="1" rounded="lg">
              <v-list>
                <v-list-item
                  v-for="(item, index) in items"
                  :key="index"
                  :to="item.to"
                  nuxt
                  exact
                >
                  {{ item.title }}
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>
          <v-col cols="8">
            <v-sheet elevation="1" rounded="lg">
              <v-container>
                <nuxt />
              </v-container>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  components: {
    Header
  },
  data() {
    return {
      items: [
        {
          title: "Practice",
          to: "/practice",
          component: "practice/index.vue"
        },
        {
          title: "Typography",
          to: "/practice/typography",
          component: "practice/Typhography.vue"
        },
        {
          title: "Buttons",
          to: "/practice/buttons",
          component: "practice/Buttons.vue"
        },
        {
          title: "Lists",
          to: "/practice/Lists",
          component: "practice/Lists.vue"
        },
        {
          title: "Layout",
          to: "/practice/layout",
          component: "practice/layouts.vue"
        }
      ]
    };
  }
};
</script>
