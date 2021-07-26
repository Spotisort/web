<template>
  <div>
    <p>{{ this.$auth.loggedIn }}</p>
    <p>{{ JSON.stringify(this.$auth.user) }}</p>
  </div>
</template>
