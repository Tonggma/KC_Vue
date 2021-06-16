<template>
  <div id="side">
    <aside>
      <ul class="sideUl">
        <li class="contact"><a class="contactme">联系<br />客服</a></li>
        <hr />
        <li class="buy"><a class="taobao" :href="taobaoUrl">购买<br />机票</a></li>
        <hr />
        <li class="buy2"><a class="taobao" :href="taobaoUrl">购买<br />门票</a></li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  name: "Vside",
  data: function () {
    return {
      taobaoUrl: "http://www.taobao.com",
    };
  },
};
</script>

<style>
#side {
  float: left;
  position: fixed;
  top: 300px;
  height: 180px;
  width: 60px;
  background: rgb(34, 33, 33);
}
aside {
  width: auto;
  height: auto;
}
.sideUl {
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
  color: white;
  overflow-x: initial;
  padding-top: 10px;
}
.taobao,.contactme {
  text-decoration: none;
  cursor: pointer;
  color: white;
}
</style>
