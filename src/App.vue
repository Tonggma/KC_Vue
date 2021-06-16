<template>
  <div id="app">
    <Vheader></Vheader>
    <Vaside></Vaside>
    <showImg></showImg>
    <Vbody></Vbody>
    <!-- <videoBackground></videoBackground> -->
    <!-- <naviBar></naviBar> -->
  </div>
</template>

<script>
import Vaside from "./components/Vaside.vue";
import Vheader from "./components/Vheader.vue";
import showImg from "./components/showImg.vue";
import Vbody from "./components/Vbody.vue";
// import Vfooter from "./components/Vfooter.vue";
// import videoBackground from "./components/videoBackground.vue";
// import naviBar from "./components/naviBar.vue";
// import timeCounter from "./components/timeCounter.vue";

export default {
  name: "App",
  components: {
    Vheader: Vheader,
    Vaside: Vaside,
    showImg: showImg,
    Vbody: Vbody,
    // Vfooter: Vfooter,
    // videoBackground: videoBackground,
    // naviBar: naviBar,
    // timeCounter: timeCounter,
  },
  data: function () {
    return {};
  },
  computed: {},
  methods: {},
};
</script>

<style>
body {
  margin: 0;
}
</style>
