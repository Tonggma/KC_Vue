<template>
  <div id="show">
    <img class="showimg" :src="arryImg[index]" />
    <div class="icon">
      <img class="sub" :src="subImg" alt="" @click="sub" />
    </div>
    <div class="icon2">
      <img class="add" :src="addImg" alt="" @click="add" />
    </div>
  </div>
</template>

<script>
import img1 from "../../public/img/cdxy1.jpg";
import img2 from "../../public/img/cdxy2.jpg";
import img3 from "../../public/img/cdxy3.jpg";
import img4 from "../../public/img/cdxy4.jpg";
import img5 from "../../public/img/cdxy5.jpg";
export default {
  name: "ShowImg",
  data() {
    return {
      arryImg: [img1, img2, img3, img4, img5],
      addImg: require("../../public/qian.png"),
      subImg: require("../../public/tui.png"),
      index: 0,
    };
  },
  mounted: function() {
    this.autoChangeImg();
  },
  methods: {
    autoChangeImg: function () {
      setInterval(this.index++,1000)
    },
    add: function () {
      if (this.index < 4) this.index++;
      else alert("已经是最后一张了");
    },
    sub: function () {
      if (this.index > 0) this.index--;
      else alert("已经是第一张了");
    },
  },
};
</script>

<style>
#show {
  width: 1280px;
  height: 500px;
  margin: 0 auto;
  margin-top: 20px;
}
.showimg {
  display: block;
  width: 1280px;
  height: 500px;
}
.icon,
.icon2 {
  float: left;
  position: absolute;
  display: block;
  width: 35px;
  height: 35px;
  cursor: pointer;
}
.icon {
  margin-left: 1248px;
}
.sub {
}
</style>
