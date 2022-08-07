<template>
  <div id="building">
    <div class="time">
      {{ msg }}
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      msg: "",
    };
  },
  created() {
    const _this = this;
    console.log(_this);
    setInterval(function () {
      let today = new Date();
      _this.msg =
        today.getFullYear() +
        "年" +
        parseInt(today.getMonth() + 1) +
        "月" +
        today.getDate() +
        "日" +
        "\xa0" +
        today.getHours() +
        "时" +
        today.getMinutes() +
        "分" +
        today.getSeconds() +
        "秒";
    }, 1000);
  },
};
</script>

<style>
#app {
  margin-top: 0px;
}

body {
  margin: 0;
  padding: 0;
  border: 0;
}

#building {
  background: url("background.jpeg");
  width: 100%;
  height: 100%;
  position: fixed;
  background-size: 100% 100%;
}

.time {
  text-align: center;
  font-size: 36px;
  margin-top: 100px;
}
</style>
