<template>
    <nav class="side-menu">
      <div class="head-area">
        <img class="head-img" v-bind:src="headSrc">
      </div>
      <div class="menu-div">
        <ul>
          <li v-for="item in menus">
              <a v-bind:href="item.url">
                <i class="fa fa-lg" v-bind:class="item.icon"></i>
                <span class="nav-text">{{item.text}}</span>
              </a>
          </li>
          <!--<li>-->
            <!--<a href="#">-->
              <!--<i class="fa fa-space-shuttle fa-lg"></i>-->
              <!--<span class="nav-text">Space Shuttle</span>-->
            <!--</a>-->
          <!--</li>-->
          <!--<li>-->
            <!--<a href="#">-->
              <!--<i class="fa fa-youtube-play fa-lg"></i>-->
              <!--<span class="nav-text">Youtube Play</span>-->
            <!--</a>-->
          <!--</li>-->
          <!--<li>-->
            <!--<a href="#">-->
              <!--<i class="fa fa-envira fa-lg"></i>-->
              <!--<span class="nav-text">Envira</span>-->
            <!--</a>-->
          <!--</li>-->
          <!--<li>-->
            <!--<a href="#">-->
              <!--<i class="fa fa-facebook fa-lg"></i>-->
              <!--<span class="nav-text">Facebook</span>-->
            <!--</a>-->
          <!--</li>-->
          <!--<li>-->
            <!--<a href="#">-->
              <!--<i class="fa fa-github fa-lg"></i>-->
              <!--<span class="nav-text">Github</span>-->
            <!--</a>-->
          <!--</li>-->
          <!--<li>-->
            <!--<a href="#">-->
              <!--<i class="fa fa-google-plus fa-lg"></i>-->
              <!--<span class="nav-text">Google Plus</span>-->
            <!--</a>-->
          <!--</li>-->
        </ul>
      </div>
    </nav>
</template>

<script>
    export default {
      name: "SideSliderMenu",
      props: ['menuList','headImageSrc'],
      watch: {
        menuList: {
          handler: function (newData, oldData) {
            this.menus = newData;
          },
          immediate: true
        },
        headImageSrc:{
          handler:function (newData,oldData) {
            this.headSrc = newData;
          },
          immediate: true
        }
      },
      data(){
        return{
          menus:[],
          headSrc: "#"
        }
      }
    }
</script>

<style scoped>

  .side-menu {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 55px;//TODO
    height: 100%;
    background: #f2f2f2;
    border-right: 1px solid #E5E5E5;
    overflow: hidden;
    box-shadow: 2px 2px 15px rgba(244, 255, 192, 0.61);
    transition: width .14s linear;
    -webkit-transition: width .14s linear;
    -o-transition: width .14s linear;
  }
  .head-area{
    display: flex;
    display: -webkit-flex;
    width: 255px;
    height: 20%;
    background: rgba(255, 255, 255, 0.65);
    justify-content: center;
    align-items: center;
  }

  .head-area>img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
  }
  .fa {
    display: table-cell;
    text-align: center;
    vertical-align: middle;
    /*height: 100%;*/
  }
  .menu-div>ul {
    -webkit-padding-start: 0;
    padding-left: 0;
    list-style-type: none;
  }
  .menu-div>ul li{
    display: block;
    width: 250px;
    height: 40px;
    list-style: none;
    border-bottom: 2px solid #F0F0F0;
    /*margin-left: 0;*/
    /*vertical-align: middle;*/
  }
  .menu-div>ul li>a {
    display: table;
    /*position: relative;*/
    width: 255px;
    height: 100%;
    text-decoration: none;
    color: #959595;
    vertical-align: middle;
    border-collapse: collapse;
    border-top: 1px solid #F0F0F0;
    box-shadow: 0 1px 1px #FAFAFA;
  }
  .nav-text{
    position: relative;
    display: table-cell;
    vertical-align: middle;
    width: 190px;
  }

  nav:hover{
    width: 255px;

  }
  .menu-div>ul li>a:hover {
    background-image: -webkit-gradient(linear, 0% 0%, 100% 100%, color-stop(0%, rgba(168, 255, 136, 0.31)), color-stop(100%, rgba(168, 255, 136, 0.8)));
    background-image: -o-linear-gradient(rgba(168, 255, 136, 0.31),rgba(168, 255, 136, 0.8));
    background-image: linear-gradient(rgba(168, 255, 136, 0.31), rgba(168, 255, 136, 0.8));
    background-image: -webkit-linear-gradient(rgba(168, 255, 136, 0.31), rgba(168, 255, 136, 0.8));
  }

</style>
