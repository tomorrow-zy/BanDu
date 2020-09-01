<template>
  <div class="bookcard">
    <img class="bookcard-picture" src="/static/index/u107.png"/>
    <div class="bookcard-text">书名</div>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.bookcard{
  margin-right: 13px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.bookcard-picture{

  width: 84px;
  height: 120px;
  border: 0.5px solid black;
  border-radius: 5px;
}
.bookcard-text{
  margin-top: 13px;
  height: 10px;
  line-height: 10px;
  text-align: center;
  font-size: 16px;
  font-weight: 30;
}
</style>