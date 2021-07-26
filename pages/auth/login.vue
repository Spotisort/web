<template>
  <div>
    <button @click='signIn()'>Login</button>
  </div>
</template>

<script>
export default {
  methods: {
    signIn() {
      this.$auth.loginWith('spotify')
    }
  }
}
</script>