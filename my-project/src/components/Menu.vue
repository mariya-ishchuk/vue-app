<template>
    <div class='cb-top-line'>
        <div class='cb-step'
            v-for='item in menuItems'
            :key='item.id'
            :class="{ 'cb-step--current': activeMenuItemId === item.id }"
            @click='onMenuItemClick(item.id)'>
            <p>
                <span>{{item.id}}</span>
                {{item.text}}
            </p>
        </div>
    </div>
</template>

<script>
const menuItems = [
    { id: 1, text: 'Image' },
    { id: 2, text: 'Frame' },
    { id: 3, text: 'Header' },
    { id: 4, text: 'FingerPrints' }
]

export default {
  name: 'menu',
  data () {
    return {
      menuItems: menuItems,
      activeMenuItemId: menuItems[0].id
    }
  },
  methods: {
    onMenuItemClick: function (id) {
      this.activeMenuItemId = id
      this.$emit('select', id)
    }
  }
}
</script>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped>
.cb-top-line {
  height: 60px;
  line-height: 60px;
  width: 640px;
  overflow: hidden;
  border-bottom: 1px solid rgba(126, 113, 101, 0.2);
}
.cb-top-line p {
  margin: 0;
  line-height: 60px;
}
.cb-step {
  color: #b2aaa3;
  float: left;
  width: 160px;
  font-size: 12px;
  cursor: pointer;
}
.cb-step:first-child p:before {
  border-left: none;
}
.cb-step p:before {
  content: "";
  display: inline-block;
  border-left: 1px solid rgba(126, 113, 101, 0.2);
  margin-right: 20px;
  line-height: 60px;
  height: 24px;
  vertical-align: middle;
}
.cb-step span {
  font-size: 18px;
  margin-right: 5px;
  font-family: FS-medium;
}
.cb-step--current {
  color: #7e7165;
  font-family: FS-bold;
}
</style>
