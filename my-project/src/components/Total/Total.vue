<template>
    <div class="cb-bottom-line">
        <div class="cb-total">
            <span class="cb-total__text">Стоимость:</span><span class="cb-total__amount"> 550</span>
            <span class="cb-total__currency"> грн</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Total',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cb-bottom-line {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 640px;
  height: 90px;
  text-align: right;
  border-top: 1px solid rgba(126,113,101,0.2);
}
.cb-total {
  height: 90px;
  display: inline-block;
  padding: 0;
  margin: 0;
  margin-right: 20px;
  line-height: 90px;
}
.cb-total__text {
  font-size: 16px;
}
.cb-total__amount {
  color: #8dbc55;
  font-size: 60px;
  font-family: FS-bold;
}
.cb-total__currency {
  color: #8dbc55;
  font-size: 18px;
}

</style>