<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-search">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="hearder-right">
       南京<span class="iconfont">&#xe600;</span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.header {
  width: 100%;
  line-height: .88rem;
  background: #00bcd4;
  color: #fff;
  font-size: .36rem;
  display: flex;
}

.header-left{
  width: .4rem;
  padding: 0 .2rem;
  text-align: center;
  font-weight: bold;
}
.header-search{
  flex: 1;
  background: #fff;
  height: .6rem;
  margin: .15rem .2rem;
  border-radius: .1rem;
  color: #e4e7ea;
  line-height: .6rem;
  font-size: .28rem;
  padding-left: .1rem;
}

.header-right{
  font-size:.20rem ;
  padding: 0 .2rem;
  padding-right: .1rem;
}

</style>
