<template>
  <div class="error-page">
    <component :is="errorPage" :error="error" />
  </div>
</template>
<script>
import error404 from '~/components/error/404.vue'
import error403 from '~/components/error/403.vue'
import error500 from '~/components/error/500.vue'
export default {
  name: 'NuxtError',
  layout: 'startpage',
  props: {
    error: {
      type: Object,
      default: () => {}
    }
  },
  computed: {
    errorPage() {
      if (this.error.statusCode === 404) {
        return error404
      }
      if (this.error.statusCode === 403) {
        return error403
      }
      // catch everything else
      return error500
    }
  }
}
</script>

<style scoped>
.error-page {
  text-align: center;
}
s .error-page a {
  text-decoration: none;
  color: $legato-color;
}

.error-page a:hover,
.error-page a:active {
  color: salmon;
}
.intro {
  height: 150px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}
</style>
