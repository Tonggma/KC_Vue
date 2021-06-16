<template>
  <div id="vWindow">

  </div>
</template>

<script>
export default {
  name: "timer",
  data() {
    return {
      targetHour: 15,
      targetMin: 0,
      targetSec: 0,
    }
  },
  mounted() {
      this.getTime();
      this.timer();
  },
  computed: {
      timer: function() {
          const H_value=this.targetHour-this.hour;
          const M_value=this.targetMin-this.minute;
          const S_value=this.targetSec-this.second;
      }
  },
  methods: {
      getTime: function() {
          const date = new Date;
          const hour = date.getHours;
          const minute = date.getMinutes;
          const second = date.getSeconds;
          //获取时间
      }
  }
}
</script>

<style>

</style>