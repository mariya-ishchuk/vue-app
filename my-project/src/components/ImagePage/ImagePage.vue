<template>
  <div class="cb-item">
      <p class="cb-item__title">
          Выберите изображение
      </p>
      <p class="cb-item__text">
          для начала выберите основу, саму картину, на которую вы и гости вашего праздника будете
          наносить отпечатки пальцев с пожеланиями
      </p>
      <div class="cb-item-pics">

          <div class="cb-item-pic">
              <img src="img/pics/01.jpg" alt="Картинка №1" title="Картинка №1" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/02.jpg" alt="Картинка №2" title="Картинка №2" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/03.jpg" alt="Картинка №3" title="Картинка №3" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/04.jpg" alt="Картинка №4" title="Картинка №4" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/05.jpg" alt="Картинка №5" title="Картинка №5" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/06.jpg" alt="Картинка №6" title="Картинка №6" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/07.jpg" alt="Картинка №7" title="Картинка №7" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/08.jpg" alt="Картинка №8" title="Картинка №8" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/09.jpg" alt="Картинка №9" title="Картинка №9" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/10.jpg" alt="Картинка №10" title="Картинка №10" width="176"
                    height="220">
          </div>
          <div class="cb-item-pic">
              <img src="img/pics/11.jpg" alt="Картинка №11" title="Картинка №11" width="176"
                    height="220">
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'ImagePage',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cb-item {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  width: 640px;
  padding: 29px 30px 0 30px;
  height: 450px;
  float: left;
}
.cb-item__title {
  font-size: 24px;
  font-family: FS-medium;
  line-height: 42px;
  margin: 0;
}
.cb-item__text {
  font-size: 14px;
  line-height: 22px;
  margin-top: 0;
}
.cb-item-pics,
.cb-item-borders,
.cb-item-marks {
  height: 320px;
  overflow: auto;
  margin-left: -6px;
  margin-right: -12px;
}
.cb-item-marks {
  height: 298px;
  margin-right: -20px;
}
.cb-item-pic {
  position: relative;
  height: 200px;
  width: 180px;
  float: left;
  margin: 6px 6px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  overflow: hidden;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  background-color: #fff;
  cursor: pointer;
  -webkit-transition: box-shadow 0.2s;
  -moz-transition: box-shadow 0.2s;
  -ms-transition: box-shadow 0.2s;
  -o-transition: box-shadow 0.2s;
  transition: box-shadow 0.2s;
}
.cb-item-pic.current {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.cb-item-pic.current:after {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  content: '';
  display: block;
  -webkit-box-shadow: 0 0 0 0, 0 0 0 5px rgba(141,188,85,0.7) inset;
  box-shadow: 0 0 0 0, 0 0 0 5px rgba(141,188,85,0.7) inset;
}
.cb-item-pic.current:hover {
  -webkit-box-shadow: 0 4px 12px 0 rgba(0,0,0,0.13);
  box-shadow: 0 4px 12px 0 rgba(0,0,0,0.13);
}
.cb-item-pic img {
  margin-top: -10px;
  margin-left: 2px;
  height: 220px;
  width: 176px;
}
.cb-item-pic:hover {
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 4px 12px 0 rgba(0,0,0,0.13);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 4px 12px 0 rgba(0,0,0,0.13);
}
.cb-item-border {
  position: relative;
  height: 200px;
  width: 180px;
  float: left;
  margin: 6px 6px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  overflow: hidden;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2) inset;
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2) inset;
  background-color: #fff;
  cursor: pointer;
  -webkit-transition: box-shadow 0.3s;
  -moz-transition: box-shadow 0.3s;
  -ms-transition: box-shadow 0.3s;
  -o-transition: box-shadow 0.3s;
  transition: box-shadow 0.3s;
}
.cb-item-border.current {
  -webkit-box-shadow: 0 0 0 5px rgba(141,188,85,0.7) inset;
  box-shadow: 0 0 0 5px rgba(141,188,85,0.7) inset;
}
.cb-item-border.current:hover {
  -webkit-box-shadow: 0 0 0 5px rgba(141,188,85,0.7) inset, 0 4px 12px 0 rgba(0,0,0,0.13);
  box-shadow: 0 0 0 5px rgba(141,188,85,0.7) inset, 0 4px 12px 0 rgba(0,0,0,0.13);
}
.cb-item-border img {
  margin-top: 25px;
  margin-left: 30px;
  height: 150px;
  width: 120px;
}
.cb-item-border:hover {
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2) inset, 0 4px 12px 0 rgba(0,0,0,0.13);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2) inset, 0 4px 12px 0 rgba(0,0,0,0.13);
}
.cb-item-border__prev {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -25px;
  margin-left: -25px;
  display: none;
  height: 50px;
  width: 50px;
  -webkit-border-radius: 25px;
  border-radius: 25px;
  -webkit-transform: scale(0.8);
  -moz-transform: scale(0.8);
  -ms-transform: scale(0.8);
  -o-transform: scale(0.8);
  transform: scale(0.8);
  opacity: 0.15;
  -webkit-transition: transform 0.3s, opacity 0.3s;
  -moz-transition: transform 0.3s, opacity 0.3s;
  -ms-transition: transform 0.3s, opacity 0.3s;
  -o-transition: transform 0.3s, opacity 0.3s;
  transition: transform 0.3s, opacity 0.3s;
  background: transparent url("/img/ico.preview.png") 0 0 no-repeat;
}
.cb-item-border__prev:hover {
  -webkit-transform: scale(1);
  -moz-transform: scale(1);
  -ms-transform: scale(1);
  -o-transform: scale(1);
  transform: scale(1);
  opacity: 0.3;
  -webkit-box-shadow: 0 4px 12px 0 rgba(0,0,0,0.3);
  box-shadow: 0 4px 12px 0 rgba(0,0,0,0.3);
}
.cb-item-border__prev:first-of-type {
  display: block;
}
.cb-item-mark {
  height: 136px;
  width: 136px;
  float: left;
  margin: 6px 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  overflow: hidden;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  background-color: #fff;
  position: relative;
}
.cb-item-mark input {
  position: absolute;
  top: -20px;
  left: -20px;
}
.cb-item-mark input + label {
  -webkit-box-shadow: none;
  box-shadow: none;
  -webkit-transition: box-shadow 0.3s;
  -moz-transition: box-shadow 0.3s;
  -ms-transition: box-shadow 0.3s;
  -o-transition: box-shadow 0.3s;
  transition: box-shadow 0.3s;
}
.cb-item-mark input:checked + label {
  -webkit-box-shadow: 0 0 0 5px rgba(141,188,85,0.7) inset;
  box-shadow: 0 0 0 5px rgba(141,188,85,0.7) inset;
}
.cb-item-mark label {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 3;
  cursor: pointer;
  display: block;
}
.cb-item-mark img {
  margin-top: 0px;
  margin-left: 0px;
  height: 136px;
  width: 136px;
}
.cb-item-mark:hover {
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 4px 12px 0 rgba(0,0,0,0.13);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 4px 12px 0 rgba(0,0,0,0.13);
}
.mark-ico {
  display: inline-block;
  line-height: 30px;
  margin-right: 4px;
  vertical-align: middle;
}
.mark-ico span {
  display: inline-block;
  height: 14px;
  width: 14px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
}
.cb-item__line {
  margin-bottom: 20px;
}
.cb-item__line input {
  height: 40px;
  width: 250px;
  margin-right: 15px;
  padding-left: 20px;
  padding-right: 20px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-border-radius: 16px;
  border-radius: 16px;
  border: none;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2) inset;
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2) inset;
}
.cb-item__line input:focus {
  outline: none;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.7) inset;
  box-shadow: 0 0 0 1px rgba(126,113,101,0.7) inset;
}
.cb-item__line input.not-valid {
  -webkit-box-shadow: 0 0 0 1px rgba(255,69,69,0.8) inset;
  box-shadow: 0 0 0 1px rgba(255,69,69,0.8) inset;
}
.cb-item__line .error {
  color: #ff4545;
  font-size: 14px;
  display: inline-block;
  vertical-align: middle;
  height: 40px;
  width: 280px;
}
.cb-item__line--btns {
  float: left;
  height: 40px;
  vertical-align: middle;
  margin-right: 15px;
  margin-top: 10px;
}
.cb-item__line--result {
  height: 40px;
  margin-left: 15px;
  margin-top: 30px;
  font-size: 24px;
}
.cb-item__line--result .ariston {
  font-size: 17px;
}
.cb-item__line--result .brody {
  font-size: 20px;
}

</style>
