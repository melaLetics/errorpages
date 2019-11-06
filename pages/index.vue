<template>
  <section class="section">
    <button @click="onCallError(500)">Call 500 error</button>
    <button @click="onCallError(404)">Call 404 error</button>
    <button @click="onCallError(403)">Call 403 error</button>
  </section>
</template>

<script>
export default {
  name: 'HomePage',
  methods: {
    onCallError(myError) {
      const error = new Error('You caused a ' + myError + ' error')
      error.statusCode = myError
      throw error
    }
  }
}
</script>
