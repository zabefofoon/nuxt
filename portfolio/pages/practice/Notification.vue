<template>
  <div>
    <v-container>
      <h1 class="headline font-weight-bold">Notification</h1>
      <p class="body-1">vuetify-dialog 모듈을 사용해보자.</p>
    </v-container>
    <v-container>
      <hr class="contour" />
      <h2 class="title font-weight-bold">$dialog.notify</h2>
      <p class="body-1">
        $dialog.notify.[info || warning || error || success]<br/>
        https://www.npmjs.com/package/vuetify-dialog 보고 활용하자.
      </p>
      <div class="code-box">
        <v-btn @click="showDialogInfo">Info</v-btn>
        <v-btn @click="showDialogWarn">warning</v-btn>
        <v-btn @click="showDialogErr">Info</v-btn>
        <v-btn @click="showDialogSuccess">Success</v-btn>
      </div>
    </v-container>
  </div>
</template>
<script>
export default {
  methods: {
    showDialogInfo() {
      this.$dialog.notify.info("Info", {
        position: "top-right",
        timeout: 5000
      })
    },
    showDialogWarn() {
      this.$dialog.notify.warning("Warn", {
        position: "top-right",
        timeout: 5000
      })
    },
    showDialogErr() {
      this.$dialog.notify.error("Error", {
        position: "top-right",
        timeout: 5000
      })
    },
    showDialogSuccess() {
      this.$dialog.notify.success("Success", {
        position: "top-right",
        timeout: 5000
      })
    }
  }
}
</script>
