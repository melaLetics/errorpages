<template>
  <div class="error-500">
    <h1>Oops, something went wrong!</h1>
    <p>{{ error.message }}</p>
    <p>Back to <a href="/">safety</a>!</p>
  </div>
</template>
<script>
export default {
  name: 'Error500',
  props: {
    error: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
