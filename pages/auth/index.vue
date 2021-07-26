<template>
  <div>
    <button @click='signIn()'>Login</button>
  </div>
</template>

<script>
export default {
  methods: {
    signIn() {
      const params = new URLSearchParams()
      params.append('client_id', process.env.spotifyClientId)
      params.append('response_type', 'code')
      params.append('redirect_uri', process.env.spotifyRedirectUri)
      params.append('scope', 'playlist-modify-public playlist-modify-private')
      // params.append('state', 'state')

      window.location.href = `https://accounts.spotify.com/authorize?${params.toString()}`
    }
  }
}
</script>