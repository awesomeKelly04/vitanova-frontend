<template>
  <v-overlay v-if="loading" v-show="message">
    <v-progress-circular :size="100" color="#F56C08" indeterminate>
      <span class="loader-text">{{message}}</span>
    </v-progress-circular>
  </v-overlay>
</template>

<script>
export default {
  name: "Loader",
  props: {
    loading: {
      type: Boolean
    },
    message: {
      type: String
    }
  }
};
</script>

<style scoped>
.v-overlay {
  background-color: transparent !important;
}
.loader-text {
  font-size: 40px;
  white-space: nowrap;
}
</style>