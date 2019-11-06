<template>
  <div class="error-404">
    <h1>This page does not exist</h1>
    <p>The link you clicked on my be broken or no longer exist.</p>
    <p>{{ error.message }}</p>
    <p>Back to <a href="/">safety</a>!</p>
  </div>
</template>
<script>
export default {
  name: 'Error404',
  props: {
    error: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
