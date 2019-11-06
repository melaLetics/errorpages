<template>
  <div class="error-404">
    <h1>Forbidden</h1>
    <p>You do not have the permission to perform this action.</p>
    <p>{{ error.message }}</p>
    <p>Back to <a href="/">safety</a>!</p>
  </div>
</template>
<script>
export default {
  name: 'Error403',
  props: {
    error: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
