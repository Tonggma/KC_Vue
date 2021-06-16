<template>
  <div id="navibar">
    <form id="bar">
      <input id="naviBar1" v-model="msg" type="text" class="searchBar" />
      <input class="submit" type="image" :src="bgSrc" @click="getValue" />
    </form>
  </div>
</template>

<script>
export default {
  name: "NaviBar",
  data: function () {
    return {
      msg: "",
      bgSrc: require("./../../public/search.png"),
    };
  },
  methods: {
    getValue: function () {
      window.open("https://www.baidu.com/s?wd=" + this.msg);
    },
    // getBgImg: function() {
    //     var classs=document.getElementById("submit");
    //     classs.style.backgroundImage=this.bgSrc;
    // }
  },
};
</script>

<style>
#naviBar {
  position: absolute;
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
</style>
