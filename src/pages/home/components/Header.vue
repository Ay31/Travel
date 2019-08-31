<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      input
    </div>
    <div class="header-right">
        city
      <span class="iconfont arrow-icon">&#xe62d;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader"
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
.header {
  display: flex;
  background: $bgColor;
  color: #ffffff;
  line-height: 0.86rem;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      font-size: 0.2rem;
      text-align: center;
    }
  }

  .header-input {
    padding-left : .2rem
    flex: 1;
    margin-top: 0.12rem;
    margin-left: 0.2rem;
    height: 0.64rem;
    line-height: 0.64rem;
    border-radius: 0.1rem;
    background: #fff;
    color: #ccc;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
    .arrow-icon {
        font-size : .2rem
    }
  }
}
</style>