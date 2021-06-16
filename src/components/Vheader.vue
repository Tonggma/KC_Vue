<template>
  <div id="div">
    <header>
      <div id="head">
        <div id="head-logo">
          <img id="logo" :src="imgSrc" alt="logo" @click="refresh" />
          <img class="Aimg" :src="imgSrc2" alt="img" />
        </div>
        <ul id="menu">
          <li class="nav1"><a class="link" @click="refresh">首页</a></li>
          <li class="nav2"><a class="link">购买</a></li>
          <li class="nav3"><a class="link">图片</a></li>
          <li class="nav4"><a class="link">视频</a></li>
          <li class="nav5"><a class="link">关于</a></li>
        </ul>
        <div id="naviBar">
          <input id="naviBar1" v-model="msg" type="text" class="searchBar" />
          <input class="submit" type="image" :src="bgSrc" @click="getValue" />
          <span class="log" @click="notice">登录 | 注册</span>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
// import naviBar from "./naviBar.vue";
export default {
  name: "Vheader",
  components: {},
  data: function () {
    return {
      imgSrc: require("./../../public/logo.png"),
      imgSrc2: require("./../../public/rick.gif"),
      msg: "",
      bgSrc: require("./../../public/search.png"),
      url: [],
    };
  },
  methods: {
    refresh: function () {
      location.reload();
    },
    getValue: function () {
      window.open("https://www.baidu.com/s?wd=" + this.msg);
    },
    notice: function () {
      alert("该功能未开放");
    },
  },
};
</script>

<style>
header {
  width: 100%;
  height: 90px;
}
#head {
  padding-left: 100px;
  height: 90px;
  background-color: rgba(167, 167, 167, 0.945);
}
#head-logo {
  float: left;
}
#logo {
  position: relative;
  width: 230px;
  height: 86px;
  cursor: pointer;
}
#menu {
  display: inline;
  list-style: none;
  float: left;
  margin: 0;
  height: 74px;
  padding-left: 200px;
}
.nav1,
.nav2,
.nav3,
.nav4,
.nav5 {
  position: relative;
  float: left;
  font-size: 24px;
  width: 80px;
  height: 80px;
  text-align: center;
  line-height: 80px;
  margin-left: 8px;
  margin-right: 8px;
}
.nav1:hover,
.nav2:hover,
.nav3:hover,
.nav4:hover,
.nav5:hover {
  background-color: rgb(163, 193, 228);
  cursor: pointer;
}
.link {
  text-decoration: none;
  color: black;
}
#naviBar {
  display: inline;
  position: relative;
  left: 300px;
  top: 24px;
}
.searchBar {
  width: 150px;
  height: 20px;
}
.submit {
  border: 0;
  width: 20px;
  height: 20px;
  display: inline-block;
  position: relative;
  top: 5px;
  right: 22px;
}
.log {
  color: brown;
  cursor: pointer;
}
.Aimg {
  float: right;
  width: 90px;
  height: 88px;
  margin-left: 20px;
}
</style>
