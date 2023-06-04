<template>
  <SignInView />
</template>

<script>
import SignInView from "./views/SignInView.vue"

export default {
  name: 'App',
  components: {
    SignInView
  }
}
</script>

<style lang="scss">
body {
  margin: 0% ;
}
#app {
  font-family: 'Geologica', sans-serif;
  font-weight: lighter;
}
</style>
