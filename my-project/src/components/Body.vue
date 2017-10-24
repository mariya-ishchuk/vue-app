<template>
  <div>
    <transition name="fade">
      <div v-if='id == 1'>
        <ImagePage />
      </div>
    </transition>
    <transition name="fade">
      <div v-if='id == 2'>
          <FramePage />
      </div>
    </transition>
    <transition name="fade">
      <div v-if='id == 3'>
          <HeadingPage />
      </div>
    </transition>
    <transition name="fade">
      <div v-if='id == 4'>
          <FingerprintsPage />
      </div>
    </transition>
    <div class="cb-wrapper">
      <div id="cb-items" class="cb-item1"></div>
    </div>
  </div>
</template>

<script>
import ImagePage from './ImagePage/ImagePage'
import FramePage from './FramePage/FramePage'
import HeadingPage from './HeadingPage/HeadingPage'
import FingerprintsPage from './FingerprintsPage/FingerprintsPage'

export default {
  name: 'Body',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  props: ['id'],
  components: {
    ImagePage,
    FramePage,
    HeadingPage,
    FingerprintsPage
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
