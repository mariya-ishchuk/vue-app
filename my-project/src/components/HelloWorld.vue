<template>
  <div>
    <Menu v-on:select="setBody"/>
    <Body :id='id'/>
  </div>
</template>

<script>
import Menu from './Menu.vue'
import Body from './Body.vue'

export default {
  name: 'HelloWorld',
  data () {
    return {
      id: 0,
      frame: 'frame',
      price: 'price'
    }
  },
  methods: {
    setBody: function (id) {
      this.id = id
    }
  },
  components: {
    Menu,
    Body
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
