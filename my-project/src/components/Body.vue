<template>
  <div>
    <transition name="fade">
        <p v-if="id == 1">hello</p>
    </transition>
    <div v-if='id == 1'>
        <ImagePage />
    </div>
    <div v-if='id == 2'>
        Frame
    </div>
    <div v-if='id == 3'>
        Header
    </div>
    <div v-if='id == 4'>
        Fingerprints
    </div>
  </div>
</template>

<script>
import ImagePage from './ImagePage/ImagePage'

export default {
  name: 'Body',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  props: ['id'],
  components: {
    ImagePage
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0
}
</style>
