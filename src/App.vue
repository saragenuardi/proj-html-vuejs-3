<template>
  <div id="app">
    <AppHeader />
    <AppServices />
    <AppBusiness />
    <AppPortfolio />
    <AppPricing />
    <AppBlog />
    <AppTestimonial />
    <AppSubcribeBox />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppServices from "./components/AppServices.vue";
import AppBusiness from "./components/AppBusiness.vue";
import AppPortfolio from "./components/AppPortfolio.vue";
import AppPricing from "./components/AppPricing.vue";
import AppBlog from "./components/AppBlog.vue";
import AppTestimonial from "./components/AppTestimonial.vue";
import AppSubcribeBox from "./components/AppSubcribeBox.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  name: "App",
  components: {
    AppHeader,
    AppServices,
    AppBusiness,
    AppPortfolio,
    AppPricing,
    AppBlog,
    AppTestimonial,
    AppSubcribeBox,
    AppFooter,
  },
};
</script>

<style lang="scss">
//VARIABILI

//Colori

$primary-background-color: #0a1750;
$secondary-background-color: #f1f1f1;
$primary-color: #888;
$secondary-color: #f9636b;
//utilizzo gradient per la sfumatura dei bottoni
$primary-gradient: linear-gradient(to right, #b7256e 0%, #f8626b 100%);
$secondary-gradient: linear-gradient(to right, #03a6d2 0%, #1f3e83 100%);
$gradient-hover: linear-gradient(to right, #cc396d 0%, #f9646c 100%);
$tertiary-gradient: linear-gradient(to bottom right, #020230 0%, #173270 100%);
$tertiary-color: #f4f4f4;
$color-4: #aaa;
$color-5: #69717b;
$color-6: #b6246e;

//Fonts
$font-body: "Open Sans", sans-serif;
$font-title: "Heebo", sans-serif;
$font-our-pricing: 'Montserrat', sans-serif;


//Bottons and mixin
@mixin buttons-style {
  border-radius: 25px;
  height: 40px;
  border: none;
}
@mixin flex-space-between {
  display: flex;
  justify-content: space-between;
}
@mixin flex-space-evenly {
  display: flex;
  justify-content: space-evenly;
}
@mixin our-pricing-box {
  width: 32%;
  height: 100%;
  position: relative;
  margin-top: 50px;
  border-radius: 20px;
  padding: 30px 0;
}

//RESET
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

//COMMON
body {
  font-family: $font-body;
}
.container {
  width: 1200px;
  margin: 0 auto;
}

a {
  text-decoration: none;
}

h1,
h2,
h3 {
  font-family: $font-title;
}

.weight-normal {
  font-weight: normal;
}

ul {
  list-style-type: none;
}

.clearfix::after {
  content: "";
  display: table;
  clear: both;
}

.fl {
  float: left;
}

.pink-button {
  background: $primary-gradient;
  color: #fff;
  @include buttons-style();
  width: 170px;
  @include flex-space-between();
  align-items: center;
  padding: 0 23px;
  cursor: pointer;
}

.pink-button:hover {
  background: $secondary-gradient;
}

.white-button {
  background: #fff;
  color: $secondary-color;
  @include buttons-style();
  width: 170px;
  @include flex-space-between();
  align-items: center;
  padding: 0 23px;
}

.white-button-2 {
  width: 125px;
  height: 40px;
  border-radius: 23px;
  border: none;
  background-color: #fff;
  cursor: pointer;
}

.opacity {
  background-color: rgba(0, 0, 0, 0.4);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 23px;
}

.pink-2-button {
  background: $primary-gradient;
  color: #fff;
  @include buttons-style();
  width: 150px;
  cursor: pointer;
}

.pink-2-button:hover {
  background: $secondary-gradient;
}

.blue-button {
  background: $secondary-gradient;
  @include buttons-style();
  margin-left: 16px;
  width: 150px;
  color: #fff;
  cursor: pointer;
}

.blue-button:hover {
  background: $primary-gradient;
}
//Header
header{
  background-color: $primary-background-color;
  height: 760px;
  background-image: url('./assets/images/header.png');
  background-repeat: no-repeat;
  background-size: 39%;
  background-position: 80% 45%;
  margin-bottom: 60px;

  .navbar{
    height: 90px;
    @include flex-space-between();
    align-items: center;
    color: white;
    
    &-left{

      .logo{
        height: 51px;
      }
    }
    &-right{

      li{
        padding-left: 25px;
        display: inline-block;
        font-size: 15px;
        
        a{
          color: #fff;
        }
        button{
          width: 90px;
          height: 35px;
          margin-left: 10px;
        }
        
        a{
          color: #fff;
        } 
      }
    }
  }

  .jumbotron{

    h1{
      width: 460px;
      margin-top: 140px;
      color: #fff;
      font-size: 50px;
    }
    span{
      margin: 5px 0;
    }

    p{
      margin-top: 30px;
      margin-bottom: 55px;
      width: 340px;
      color: $tertiary-color;
      font-size: 12px;
    }
  }
}

//Section SERVICES

.services {
  text-align: center;

  > span {
    color: $secondary-color;
    font-size: 13px;
  }

  h2 {
    margin: 15px 0;
  }

  p {
    color: $primary-color;
    font-size: 13px;
  }

  &-list {
    @include flex-space-evenly();
    text-align: center;

    img {
      width: 125px;
      height: 100px;
      margin-top: 100px;
    }

    h3 {
      margin-top: 30px;
      margin-bottom: 20px;
    }

    p {
      color: $primary-color;
      width: 200px;
    }
  }
  button {
    margin-top: 90px;
  }
}
//Section BUSINESS

.grow-your-business-section {
  background-color: $primary-background-color;
  height: 700px;
  color: #fff;
  margin-top: 70px;
  background-image: url("./assets/images/men-data.png");
  background-repeat: no-repeat;
  background-size: 27%;
  background-position: 20% 60%;
  margin-bottom: 60px;
  display: flex;
  align-items: center;

  .grow-your-business {
    margin-left: 650px;
    > span {
      font-size: 13px;
    }
  }

  h2 {
    width: 450px;
    margin-top: 20px;
    font-size: 50px;
  }

  p {
    width: 420px;
    margin-top: 30px;
    margin-bottom: 40px;
    color: $tertiary-color;
    font-size: 13px;
  }
}

//Section PORTFOLIO

.portfolio-section {
  background-color: $secondary-background-color;

  &-content {
    @include flex-space-between();
    align-items: flex-end;
    padding: 85px 0 60px 0;

    &-left {
      > span {
        color: $secondary-color;
        font-size: 13px;
      }

      h2 {
        font-size: 32px;
      }
    }
    &-right {
      i {
        color: $secondary-color;
        font-size: 32px;
        padding-bottom: 10px;
        margin-left: 10px;
      }
    }
  }
  &-content-img {
    @include flex-space-between();

    &-container {
      width: 375px;
      height: 300px;
      background-color: #fff;
      border-radius: 20px;

      img {
        width: 375px;
        height: 240px;
        border-radius: 20px;
      }

      &-text {
        @include flex-space-between();
        height: calc(300px - 240px);
        padding: 16px 30px;

        span {
          color: $color-4;
          font-size: 10px;
        }

        h3 {
          font-size: 14px;
        }
      }
    }

    &-container:hover {
      background: $gradient-hover;
    }
  }
  .icons-container {
    display: flex;
    justify-content: center;
    padding: 43px 0 40px 0;

    .fas:first-child {
      color: $secondary-color;
      font-size: 6px;
    }
    .fas {
      color: $primary-color;
      font-size: 6px;
      margin-left: 5px;
    }
  }
}

//Section PRICING

.our-pricing-section {
  width: 100%;
  height: 500px;
  text-align: center;
  background-color: $primary-background-color;
  padding-top: 50px;
  position: relative;

  > span {
    color: $secondary-color;
    font-size: 12px;
  }

  > h2 {
    margin: 12px 0 8px 0;
    color: #fff;
    font-size: 38px;
  }

  p {
    color: #fff;
    font-size: 13px;
    width: 37%;
    margin: 0 auto 12px auto;
  }

  .container {
    @include flex-space-between();
    position: absolute;
    left: 158px;
    margin-left: 150px;
  }

  &-box-white {
    @include our-pricing-box();
    background-color: #fff;
    overflow: hidden;

    .transparent-number {
      font-size: 260px;
      position: absolute;
      right: -13px;
      top: -87px;
      color: #000;
      opacity: 0.1;
    }

    &-top {
      position: relative;
      z-index: 1;

      h3 {
        font-size: 28px;
      }

      span {
        text-transform: uppercase;
        font-size: 12px;
      }
    }

    &-middle {
      margin-top: 33px;
      padding-bottom: 40px;
      position: relative;
      z-index: 1;

      .dollar {
        margin-right: 90px;
        font-size: 15px;
      }

      h2 {
        font-size: 80px;
        font-family: $font-our-pricing;
      }
      span {
        font-size: 12px;
      }
    }

    &-bottom {
      li {
        padding-bottom: 6px;
        font-size: 13px;
      }
      span {
        font-weight: bold;
      }
      .button-container {
        display: flex;
        justify-content: center;
        button {
          margin: 30px 0 16px 0;

          i {
            font-size: 16px;
          }
        }
      }
    }
  }
  &-box-pink {
    @include our-pricing-box();
    background: linear-gradient(to bottom, #bf2d6d 0%, #ea566d 100%);
    color: #fff;
    overflow: hidden;

    .transparent-number {
      font-size: 260px;
      position: absolute;
      right: -13px;
      top: -87px;
      color: #fff;
      opacity: 0.1;
    }

    &-top {
      position: relative;
      z-index: 1;

      h3 {
        font-size: 28px;
      }

      span {
        text-transform: uppercase;
        font-size: 12px;
      }
    }

    &-middle {
      margin-top: 31px;
      padding-bottom: 40px;
      position: relative;
      z-index: 1;

      .dollar {
        margin-right: 90px;
      }

      h2 {
        font-size: 80px;
        font-family: $font-our-pricing;
      }
      span {
        font-size: 12px;
      }
    }

    &-bottom {
      li {
        padding-bottom: 6px;
        font-size: 13px;
      }
      span {
        font-weight: bold;
      }

      .button-container {
        display: flex;
        justify-content: center;
        button {
          margin: 30px 0 16px 0;

          i {
            font-size: 16px;
          }
        }
      }
    }
  }
}
//Section BLOG
.blog-section {
  background-color: $secondary-background-color;
  height: 700px;
  padding-top: 400px;
  text-align: center;
}
> span {
  color: $secondary-color;
  font-size: 13px;
}
h2 {
  margin: 5px 0;
  font-size: 38px;
}

> p {
  color: $primary-color;
  font-size: 13px;
  width: 37%;
  margin: 0 auto;
  margin-bottom: 75px;
}

.container-section {
  @include flex-space-between();
  text-align: left;
  padding: 50px 100px;
  .left {
    @include flex-space-between();
    padding: 0 40px 30px 40px;

    background-image: url("./assets/images/headway-537308-unsplash-1380x703.jpg");
    position: relative;
    background-size: cover;
    width: 48%;
    height: 330px;
    color: #fff;
    border-radius: 23px;

    .inner-left {
      display: flex;
      align-items: flex-end;
    }

    .inner-right {
      position: relative;
      display: flex;
      align-items: flex-end;
    }

    span {
      position: relative;
      font-size: 11px;
    }
    .dash {
      margin: 0 7px;
    }
    h3 {
      position: relative;
      margin: 10px 0;
      font-size: 16px;
    }
    p {
      position: relative;
      font-size: 11px;
      width: 90%;
    }
  }
  .middle {
    width: 23%;
    height: 330px;
    background: linear-gradient(to bottom right, #020230 0%, #173270 100%);
    color: #fff;
    padding: 30px 60px 30px 42px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    border-radius: 23px;

    span {
      font-size: 11px;
    }
    .dash {
      margin: 0 7px;
    }
    h3 {
      margin: 25px 0;
      font-size: 16px;
    }
    p {
      font-size: 11px;
    }
    button {
      margin-top: 40px;
    }
  }
  .right {
    width: 23%;
    height: 330px;
    background: $tertiary-gradient;
    color: #fff;
    padding: 30px 60px 30px 42px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    border-radius: 23px;

    span {
      font-size: 11px;
    }
    .dash {
      margin: 0 7px;
    }
    h3 {
      margin: 25px 0;
      font-size: 16px;
    }
    p {
      font-size: 11px;
    }
    button {
      margin-top: 40px;
    }
  }
}

//Section TESTIMONIAL
.testimonial-section {
  text-align: center;
  padding-top: 310px;
  position: relative;

  > span {
    color: $secondary-color;
    font-size: 13px;
  }
  h2 {
    margin: 5px 0 20px 0;
    font-size: 38px;
  }

  > p {
    color: $primary-color;
    font-size: 13px;
    width: 37%;
    margin: 0 auto;
    margin-bottom: 75px;
  }

  .quotes-container {
    text-align: left;
    @include flex-space-between();

    &-box {
      width: 30%;
      position: relative;
      text-align: center;

      .quotation-mark {
        position: absolute;
        font-size: 170px;
        top: 30px;
        left: 38%;
        opacity: 0.1;
      }

      img {
        height: 60px;
        border-radius: 100%;
        border: 3px solid $color-6;
      }

      .icons {
        padding: 26px 0;
        position: relative;
        z-index: 2;
        font-size: 12px;

        .fas {
          color: $color-6;
        }
        .far {
          color: $color-6;
        }
      }

      p {
        font-size: 13px;
        padding-bottom: 20px;
      }

      .credits {
        span {
          font-size: 13px;
          font-weight: bold;
        }

        p {
          margin-top: 7px;
        }
      }
    }
  }
  .partners-img {
    display: flex;
    justify-content: space-around;
    margin-top: 140px;
    margin-bottom: 50px;

    img {
      height: 52px;
    }
    img:nth-child(2) {
      height: 30px;
      margin-top: 12px;
    }
  }

  .opacity {
    background-color: rgba(0, 0, 0, 0.5);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
}
</style>