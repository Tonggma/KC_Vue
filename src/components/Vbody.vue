<template>
  <div id="Vbody">
    <div class="discount1">
      <p>{{ title1 }}</p>
      <div>
        <label>{{ msg1 }}<br />￥{{ price1 }}</label>
        <label>{{ msg2 }}<br />￥{{ price2 }}</label>
        <label>{{ msg3 }}<br />￥{{ price3 }}</label>
      </div>
    </div>
    <div class="discount2">
      <p>{{ title2 }}</p>
    </div>
    <div class="discount3">
      <p>{{ title3 }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Vbody",
  data() {
    return {
      title1: "特价车票",
      title2: "特价机票",
      title3: "特价酒店",
      msg1: "成都→雅安",
      msg2: "成都→攀枝花",
      msg3: "成都→德阳",
      price1: 50,
      price2: 57,
      price3: 55,
    };
  },
};
</script>

<style scoped>
#Vbody {
  width: 1280px;
  height: auto;
  margin: 0 auto;
}
p {
  font-size: 25px;
  margin-bottom: 10px;
}
label {
  font-size: 18px;
  color: black;
  background: rgb(35, 214, 18);
  display: inline-block;
  padding: 30px;
  margin-right: 20px;
  width: 120px;
  height: 80px;
}
</style>
