<template>
  <v-row justify="center" align="center">
    <h1 class="text-center" v-if="error.statusCode === 404">
      {{ pageNotFound }}
    </h1>
    <h1 class="text-center" v-else>
      {{ otherError }}
    </h1>
  </v-row>
</template>

<script>
export default {
  layout: "empty",
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data() {
    return {
      pageNotFound: "404 Not Found",
      otherError: "An error occurred"
    };
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError;
    return {
      title
    };
  }
};
</script>

<style scoped>
h1 {
  font-size: 48px;
}
</style>
