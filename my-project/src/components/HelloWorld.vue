<template>
  <div>
    <Menu v-on:select="setBody"/>
    <Body :id='id'/>
  </div>
</template>

<script>
import Menu from './Menu.vue'
import Body from './Body.vue'
import Result from './Result.vue'

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
    Body,
    Result
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  color: #7e7165;
  font-size: 16px;
  line-height: 22px;
  font-family: FS-regular;
}
[v-cloak] {
  display: none;
}
body.oh {
  overflow: hidden;
}
#overlay {
  opacity: 0;
  visibility: hidden;
  background-color: #fff;
}
#overlay.active {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  visibility: visible;
  z-index: 3;
}
a {
  color: #7e7165;
  text-decoration: none;
}
a:hover {
  color: #8dbc55;
}
::selection {
  color: #fff;
  background: #8dbc55;
}
::-moz-selection {
  color: #fff;
  background: #8dbc55;
}
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
ul li {
  display: inline-block;
}
h1 {
  font-size: 32px;
  font-family: FS-bold;
  font-weight: normal;
  line-height: 50px;
  text-transform: uppercase;
  letter-spacing: 1.5px;
}
h2 {
  font-size: 32px;
  font-family: FS-regular;
  text-transform: uppercase;
  margin-top: 60px;
  margin-bottom: 30px;
  letter-spacing: 2px;
}
.dotted {
  overflow: hidden;
}
.dotted h2 {
  display: inline-block;
  position: relative;
  padding-left: 10px;
  padding-right: 10px;
  letter-spacing: 2px;
}
.dotted h2:before,
.dotted h2:after {
  position: absolute;
  top: 8px;
  height: 5px;
  width: 1000px;
  content: '';
  display: block;
  background: transparent url("/img/ico.dot.png") 0 0 repeat-x;
}
.dotted h2:before {
  right: 100%;
}
.dotted h2:after {
  left: 100%;
}
.dots {
  height: 100px;
  background: transparent url("/img/ico.dot.png") 0 center repeat-x;
}
input,
textarea {
  outline: none;
}
.menu__ul i {
  opacity: 0.3;
  display: inline-block;
  background-color: #7e7165;
}
.text-center {
  text-align: center;
}
.text-right {
  text-align: right;
}
.centered {
  margin: 0 auto;
}
.font-size-24 {
  font-size: 24px;
  line-height: 42px;
}
.font-size-14 {
  font-size: 14px;
  line-height: 22px;
}
.header {
  position: relative;
  height: 170px;
  padding-top: 10px;
  font-size: 12px;
}
.lng-search {
  height: 40px;
  line-height: 40px;
}
.lng {
  float: left;
}
.lng span {
  opacity: 0.3;
  padding-left: 17px;
  padding-right: 10px;
}
.search {
  margin-top: -3px;
  position: relative;
  margin-left: 110px;
  -webkit-border-radius: 20px;
  border-radius: 20px;
  width: 40px;
  height: 40px;
  cursor: pointer;
}
.search__icon {
  position: absolute;
  top: 8px;
  left: 8px;
  height: 20px;
  width: 23px;
  background: transparent url("/img/ico.search.png") 3px 2px no-repeat;
  -webkit-transition: transform 0.3s 1.4s, opacity 0.3s 1.4s;
  -moz-transition: transform 0.3s 1.4s, opacity 0.3s 1.4s;
  -ms-transition: transform 0.3s 1.4s, opacity 0.3s 1.4s;
  -o-transition: transform 0.3s 1.4s, opacity 0.3s 1.4s;
  transition: transform 0.3s 1.4s, opacity 0.3s 1.4s;
}
.search:hover .search__icon {
  -webkit-transform: rotate(110deg);
  -moz-transform: rotate(110deg);
  -ms-transform: rotate(110deg);
  -o-transform: rotate(110deg);
  transform: rotate(110deg);
  opacity: 0;
  -webkit-transition: transform 0.3s, opacity 0.3s 0.3s;
  -moz-transition: transform 0.3s, opacity 0.3s 0.3s;
  -ms-transition: transform 0.3s, opacity 0.3s 0.3s;
  -o-transition: transform 0.3s, opacity 0.3s 0.3s;
  transition: transform 0.3s, opacity 0.3s 0.3s;
}
.search:hover .search__line {
  opacity: 1;
  visibility: visible;
  width: 300px;
  left: -12px;
  -webkit-transition: all 0.7s 0.3s;
  -moz-transition: all 0.7s 0.3s;
  -ms-transition: all 0.7s 0.3s;
  -o-transition: all 0.7s 0.3s;
  transition: all 0.7s 0.3s;
}
.search__line {
  opacity: 0;
  visibility: hidden;
  position: absolute;
  top: 0;
  left: 150px;
  height: 40px;
  width: 0;
  padding-right: 110px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  background-color: #fff;
  -webkit-border-radius: 20px;
  border-radius: 20px;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.5) inset;
  box-shadow: 0 0 0 1px rgba(126,113,101,0.5) inset;
  -webkit-transition: all 0.7s 0.7s;
  -moz-transition: all 0.7s 0.7s;
  -ms-transition: all 0.7s 0.7s;
  -o-transition: all 0.7s 0.7s;
  transition: all 0.7s 0.7s;
}
.search__input {
  border: none;
  margin-left: 20px;
  vertical-align: middle;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  width: 100%;
  color: #7e7165;
  font-family: FS-medium;
  font-size: 16px;
  outline: none;
}
.search__submit {
  position: absolute;
  top: 0;
  right: 0;
  height: 40px;
  width: 80px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-border-radius: 20px;
  border-radius: 20px;
  color: #fff;
  font-size: 14px;
  font-family: FS-regular;
  cursor: pointer;
  background-color: #7e7165;
  border: none;
}
.search__submit:hover {
  opacity: 0.8;
}
.phones {
  padding-top: 15px;
}
.phones p {
  font-family: FS-regular;
  font-size: 18px;
  margin: 0.7em 0;
}
.logo {
  margin-top: 50px;
}
.logo img {
  display: block;
  margin: 0 auto;
}
.top-links {
  margin-top: 7px;
}
.top-links li {
  font-family: FS-regular;
}
.top-links span {
  opacity: 0.3;
  padding-left: 13px;
  padding-right: 15px;
}
.cart-area {
  margin-top: 40px;
}
.cart {
  height: 50px;
  width: 60px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  padding-top: 8px;
  padding-left: 10px;
  float: right;
  background: transparent url("/img/cart.png") 0 0 no-repeat;
  color: #b2aaa3;
  font-size: 18px;
  text-align: center;
}
.cart:hover {
  color: #fff;
  background: transparent url("/img/cart.png") 0 -51px no-repeat;
}
nav {
  border-top: 1px solid rgba(126,113,101,0.2);
  border-bottom: 1px solid rgba(126,113,101,0.2);
  height: 60px;
}
.menu {
  position: relative;
}
.menu ul {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  text-align: justify;
  padding: 0;
}
.menu ul:after {
  content: '';
  width: 100%;
  height: 0;
  line-height: 0;
  font-size: 0;
  visibility: hidden;
  display: inline-block;
}
.menu ul li {
  line-height: 60px;
  font-size: 18px;
  text-transform: uppercase;
  letter-spacing: 2.25px;
  display: inline-block;
}
.menu ul i {
  height: 5px;
  width: 5px;
  -webkit-border-radius: 50%;
  border-radius: 50%;
  line-height: 60px;
}
.menu__a {
  line-height: 60px;
  display: inline-block;
}
.menu__a--current {
  font-family: FS-bold;
  cursor: default;
}
.menu__a--current:hover {
  color: #7e7165;
}
.bb-left,
.bb-right {
  width: 280px;
  height: 306px;
  margin-top: 24px;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  overflow: hidden;
}
.bb-left {
  float: left;
  margin-left: 2px;
  -webkit-border-radius: 5px 0 0 5px;
  border-radius: 5px 0 0 5px;
}
.bb-right {
  float: right;
  margin-right: 2px;
  -webkit-border-radius: 0 5px 5px 0;
  border-radius: 0 5px 5px 0;
}
.bb-center {
  position: absolute;
  top: 7px;
  left: 50%;
  margin-left: -188px;
  height: 340px;
  width: 376px;
  overflow: hidden;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 6px 15px 0 rgba(0,0,0,0.2);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 6px 15px 0 rgba(0,0,0,0.2);
}
.catalog-page h1 {
  margin-bottom: 7px;
}
.catalog-page main p {
  font-size: 14px;
  line-height: 24px;
  margin: 0 0 35px 0;
}
.catalog__item {
  -webkit-border-radius: 5px;
  border-radius: 5px;
  overflow: hidden;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  height: 280px;
  -webkit-transition: box-shadow 0.3s;
  -moz-transition: box-shadow 0.3s;
  -ms-transition: box-shadow 0.3s;
  -o-transition: box-shadow 0.3s;
  transition: box-shadow 0.3s;
}
.catalog__item img {
  display: block;
}
.catalog__item:hover {
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 4px 12px 0 rgba(0,0,0,0.13);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2), 0 4px 12px 0 rgba(0,0,0,0.13);
}
.catalog__item:hover a {
  color: #7e7165;
}
.catalog__item .catalog__item__text {
  height: 64px;
  letter-spacing: -4px;
  padding: 0 20px;
}
.catalog__item .catalog__item__text:before {
  content: '';
  display: inline-block;
  vertical-align: middle;
  height: 100%;
  width: 0;
  margin-left: -1px;
}
.catalog__item .catalog__item__text p {
  font-size: 16px;
  line-height: 22px;
  opacity: 1;
  letter-spacing: 0;
  display: inline-block;
  vertical-align: middle;
  margin: 0;
}
.constructor-block {
  position: relative;
  height: 600px;
  width: 936px;
  margin-bottom: 40px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  -webkit-box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
  box-shadow: 0 0 0 1px rgba(126,113,101,0.2);
}
.constructor__price {
  color: #8dbc55;
  margin: 10px 0 -25px;
  text-align: center;
  letter-spacing: -1px;
}
.constructor__text {
  margin-bottom: 40px;
}
.constructor__text--small {
  margin-top: -15px;
}
.constructor__amount {
  position: relative;
  font-size: 60px;
  font-family: FS-bold;
  line-height: 90px;
  margin: 0;
  display: inline-block;
}
.constructor__currerncy {
  position: absolute;
  top: 47px;
  right: -35px;
  display: inline-block;
  font-size: 18px;
  line-height: 18px;
  font-family: FS-regular;
}
.cb-top-line {
  height: 60px;
  line-hgith: 60px;
  width: 640px;
  overflow: hidden;
  border-bottom: 1px solid rgba(126,113,101,0.2);
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
  content: '';
  display: inline-block;
  border-left: 1px solid rgba(126,113,101,0.2);
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
.cb-result {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  width: 296px;
  -webkit-border-radius: 0 5px 5px 0;
  border-radius: 0 5px 5px 0;
  background-color: #e6e3e1;
}
.cb-result p {
  margin: 0;
}
.cb-result__title {
  width: 276px;
  border-bottom: 1px solid rgba(126,113,101,0.2);
  font-size: 18px;
  font-family: FS-medium;
  height: 60px;
  line-height: 60px;
  padding-left: 20px;
  overflow: hidden;
}
.cb-result__content {
  padding: 25px 30px;
  height: 400px;
}
.cb-result__data {
  height: 30px;
  line-height: 30px;
  font-size: 16px;
  font-family: FS-regular;
}
.cb-result__data span {
  vertical-align: top;
}
.cb-result__data strong {
  display: inline-block;
  font-weight: normal;
  font-family: FS-medium;
}
.cb-result__marks {
  display: inline-block;
  width: 145px;
}
.cb-result__marks span {
  vertical-align: baseline;
}
.cb-result__object {
  position: relative;
  height: 300px;
  width: 240px;
  margin-top: 25px;
  -webkit-box-shadow: 0 2px 6px 0 rgba(0,0,0,0.13);
  box-shadow: 0 2px 6px 0 rgba(0,0,0,0.13);
}
.cb-result__border,
.cb-result__img,
.cb-result__text {
  position: absolute;
}
.cb-result__border img,
.cb-result__img img,
.cb-result__text img {
  height: 300px;
  width: 240px;
}
.cb-result__img {
  top: 0;
  left: 0;
  height: 300px;
  width: 240px;
  background-color: #fff;
}
.cb-result__border {
  top: 0;
  left: 0;
  height: 300px;
  width: 240px;
}
.cb-result__text__title,
.cb-result__text__name,
.cb-result__text__date {
  position: absolute;
  overflow: hidden;
  left: 35px;
  right: 35px;
  text-align: center;
  font-size: 14px;
  line-height: 1;
}
.cb-result__text__title.davinci,
.cb-result__text__name.davinci,
.cb-result__text__date.davinci {
  font-size: 16px;
}
.cb-result__text__title {
  top: 40px;
}
.cb-result__text__name {
  bottom: 50px;
}
.cb-result__text__name.small {
  font-size: 10px;
}
.cb-result__text__date {
  bottom: 35px;
}
.cb-result__bottom {
  height: 70px;
  padding-top: 20px;
}
.cb-button {
  display: block;
  margin: 0 auto 20px;
  height: 50px;
  width: 250px;
  -webkit-border-radius: 20px;
  border-radius: 20px;
  background-color: #8dbc55;
  border: none;
  -webkit-box-shadow: none;
  box-shadow: none;
  color: #fff;
  font-size: 18px;
  line-height: 55px;
  font-family: FS-medium;
  text-transform: uppercase;
  opacity: 0.7;
}
.cb-button.active {
  opacity: 1;
}
.cb-button.active:hover {
  background-color: #74af2d;
  -webkit-box-shadow: 0 0 0 2px #74af2d;
  box-shadow: 0 0 0 2px #74af2d;
}
.cb-button.active:active {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.cb-result__bottom .cb-next {
  display: block;
  margin: 0 auto 20px;
  height: 50px;
  width: 250px;
  -webkit-border-radius: 20px;
  border-radius: 20px;
  background-color: #8dbc55;
  color: #fff;
  font-size: 18px;
  line-height: 55px;
  font-family: FS-medium;
  text-align: center;
  text-transform: uppercase;
  opacity: 0.7;
}
.cb-result__bottom .cb-next.active {
  cursor: pointer;
  opacity: 1;
}
.cb-result__bottom .cb-next.active:hover {
  background-color: #74af2d;
  -webkit-box-shadow: 0 0 0 2px #74af2d;
  box-shadow: 0 0 0 2px #74af2d;
}
.cb-result__bottom .cb-next.active:active {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.cb-wrapper {
  position: absolute;
  top: 60px;
  left: 0;
  height: 450px;
  width: 640px;
  overflow: hidden;
}
#cb-items {
  width: 2560px;
  position: absolute;
  top: 0;
  left: 0;
  -webkit-transition: left 0.3s ease;
  -moz-transition: left 0.3s ease;
  -ms-transition: left 0.3s ease;
  -o-transition: left 0.3s ease;
  transition: left 0.3s ease;
}
#cb-items.cb-item1 {
  left: 0;
  -webkit-transition: left 0.3s ease;
  -moz-transition: left 0.3s ease;
  -ms-transition: left 0.3s ease;
  -o-transition: left 0.3s ease;
  transition: left 0.3s ease;
}
#cb-items.cb-item2 {
  left: -640px;
  -webkit-transition: left 0.3s ease;
  -moz-transition: left 0.3s ease;
  -ms-transition: left 0.3s ease;
  -o-transition: left 0.3s ease;
  transition: left 0.3s ease;
}
#cb-items.cb-item3 {
  left: -1280px;
  -webkit-transition: left 0.3s ease;
  -moz-transition: left 0.3s ease;
  -ms-transition: left 0.3s ease;
  -o-transition: left 0.3s ease;
  transition: left 0.3s ease;
}
#cb-items.cb-item4 {
  left: -1920px;
  -webkit-transition: left 0.3s ease;
  -moz-transition: left 0.3s ease;
  -ms-transition: left 0.3s ease;
  -o-transition: left 0.3s ease;
  transition: left 0.3s ease;
}
.ariston {
  font-family: 'Ariston';
}
.davinci {
  font-family: 'Davinci';
}
.brody {
  font-family: 'Brody';
}
.btn-font {
  display: inline-block;
  height: 40px;
  width: 100px;
  margin-right: 10px;
  -webkit-border-radius: 16px;
  border-radius: 16px;
  color: #8dbc55;
  font-size: 16px;
  line-height: 40px;
  text-align: center;
  -webkit-box-shadow: 0 0 0 1px #8dbc55 inset;
  box-shadow: 0 0 0 1px #8dbc55 inset;
  cursor: pointer;
}
.btn-font:last-child {
  margin-right: 0;
}
.btn-font--active {
  color: #fff;
  background-color: #8dbc55;
}
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
