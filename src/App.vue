<template lang="pug">
  #app
    sui-menu.dings(:widths="3")
      sui-menu-item
        router-link(to="/radar") Radar
      sui-menu-item Chat
      sui-menu-item Files
      sui-menu-item Whiteboard
      sui-menu-item
        router-link(to="/TodoExample") TodoExample
      sui-menu-item
        router-link(to="/WebTorrentDemo") WebTorrentDemo
      sui-menu-item
        router-link(to="/P2pDevModeInfo") p2p dev mode info

    router-view.viewport/

</template>

<script>
export default {
  name: 'App',
  data () {
    return { visible: true }
  },
  methods: {
    handleDismiss () {
      this.visible = false
      setTimeout(() => {
        this.visible = true
      }, 2000)
    }
  }
}

</script>

<style lang="sass">
#app
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  // margin-top: 60px

.dings
  position: fixed
  top: 0
  left: 0
  width: 100%
  z-index: 100
.viewport
  position: relative
  top: 46px

</style>
