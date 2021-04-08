<template>
  <div>
    <v-container>
      <h1 class="headline font-weight-bold">Loading</h1>
      <p class="body-1">Nuxt의 Loading 처리를 알아보자.</p>
    </v-container>
    <v-container>
      <hr class="contour"/>
      <h2 class="title font-weight-bold">nuxt.config</h2>
      <p class="body-1">
        nuxt.config.js에서 설정하면, global progress bar를 사용할 수 있다.<br/>
        loading: { color: "orange", height: "2px", continuous: true }<br/>
        페이지 이동할 때 표시될 수 있다.
      </p>
    </v-container>
    <v-container>
      <hr class="contour"/>
      <h2 class="title font-weight-bold">AsyncData와 Fetch Hook</h2>
      <p class="body-1">
        둘다 서버사이드에서 요청이 된다.<br/>
        asyncData: preloadData처럼 사용한다. 요청이 길어진다면, 페이지로드가 느려진다.<br/>
        fetch: fetch hook안에서 비동기 요청하면, 서버에서 요청하지만 페이지 로드가 느려지지 않는다.<br/>
        $fetchState를 통해 상태를 표시할 수 있다.<br/>
        @click="$fetch"를 통해 refresh를 할 수 있다.<br/>
        postman으로 초기 데이터를 확인할 수 있다.
      </p>
      <div class="code-box">
        {{ asyncDataText.name }}
        <template v-if="$fetchState.pending">
          Loading...
        </template>
        <template v-else>
          {{ fetchText.name }}
        </template>
        {{ mountedText.name }}<br/>
        <v-btn @click="$fetch">Refresh</v-btn>
      </div>
    </v-container>
    <v-container>
      <hr class="contour"/>
      <h2 class="title font-weight-bold">$nuxt.$loading</h2>
      <p class="body-1">
        $nuxt.$loading.start(), $nuxt.$loading.finish()로 로딩표시를 할 수 있다.
      </p>
      <div class="code-box">
        <v-btn @click="displayLoading">load</v-btn>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  async asyncData() {
    const text = await new Promise(resolve => setTimeout(() => {
      resolve({name: "World"})
    }, 200))
    return {
      asyncDataText: text
    }
  },
  data() {
    return {
      fetchText: {},
      mountedText: {}
    }
  },
  async fetch() {
    this.fetchText = await new Promise(resolve => setTimeout(() => {
      resolve({name: "Hello"})
    }, 300))
  },
  methods: {
    async setMountedText() {
      this.mountedText = await new Promise(resolve => setTimeout(() => {
        resolve({name: "Happy"})
      }, 300))
    },
    displayLoading() {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 1000)
    }
  },
  mounted() {
    this.setMountedText()
  }
}
</script>
