<template>
  <div>
    <p v-if="!this.$auth.loggedIn">Logging out</p>
    <p v-else>Logged Out</p>
  </div>
</template>

<script>
export default {
  created() {
    this.$auth.logout()
  }
}
</script>