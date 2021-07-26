<template>
  <div>
    <p v-if="!this.$auth.loggedIn">Logging in...</p>
    <p v-else>Logged In</p>
  </div>
</template>

<script>
export default {
  created() {
    this.$auth.setUserToken(this.$route.params.access_token, this.$route.params.refresh_token)
  }
}
</script>