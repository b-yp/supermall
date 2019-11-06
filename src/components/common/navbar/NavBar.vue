<template>
  <div class="navbar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>  
</template>

<script>
export default {
  
}
</script>

<style scoped>
  .navbar {
    height: 44px;
    display: flex;
    line-height: 44px;
    background: pink;
  }
  .left {
    width: 44px;
  }
  .right {
    width: 44px;
  }
  .center {
    flex: 1;
    text-align: center;
    color: white;
  }
</style>