<template>
  <div class="bottom">
      <div class="bottom-wrapper">
        <div class="home">
          <img class="home-image" src="/static/index/u14.png"/>
          <div class="home-text">首页</div>
        </div>
        <div class="shelf">
          <img class="home-image" src="/static/index/u17.png"/>
          <div class="home-text">书架</div>
        </div>
        <div class="my">
          <img class="home-image" src="/static/index/u9.png"/>
          <div class="home-text">我的</div>
        </div>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.bottom-wrapper{
  position: fixed;
  bottom: 0;
  width: 100%;
  background: #fff;
  padding: 3px 20px 5px 20px;
  display: flex;
  box-sizing: border-box;
  border-top: 1px solid #eee;
  box-shadow: 0 -2px 4px 0 rgba(0,0,0,.1);
}
.home{
  display: flex;
  flex-direction: column;
  margin-right: 123px;
}
.home-image {
  width: 30px;
  height: 30px;
}
.home-text{
  font-size: 13px;
  font-weight: 50;
  text-align: center;
}
.shelf{
  display: flex;
  flex-direction: column;
  margin-right: 123px;
}
.my{
  display: flex;
  flex-direction: column;
}
</style>