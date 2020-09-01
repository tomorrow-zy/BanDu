<template>
  <div>
    <div class="head">
      <div class="head-wrapper">
        <img class="user" src="/static/index/u103.png" @click="onMyClick"/>
        <div class="head-text">首页</div>
        <img class="message" src="/static/index/u104.png" @click="onMessageClick"/>
      </div>
    </div>
    <div class="content">
      <div class="content-wrapper">
        <Banner/>
        <div class="library">
          <div class="library-head">
            <div class="library-text">图书馆</div>
          </div>
          <div class="library-content">
            <div class="library-content-head">
              <div class="allbooks">
                <img src="/static/index/u66.png" class="bookpic">
                <div class="allbooks-text">全部书籍</div>
              </div>
              <div class="bookshelf">
                <img src="/static/index/u92.png" class="shelfpic">
                <div class="bookshelf-text">我的书架</div>
              </div>
            </div>
            <div class="library-content-book">
              <BookCard/>
              <BookCard/>
              <BookCard/>
            </div>
          </div>
        </div>
        <div class="recommend">
         <div class="recommend-head">
           <div class="recommend-text">图书推荐</div>
         </div>
         <div class="recommend-content">
            <div class="recommend-content-head">
              <div class="bookrank">
                <img src="/static/index/u27.png" class="bookrankpic">
                <div class="bookrank-text">排行榜</div>
                <div class="more">
                  <div class="more-text">更多</div>
                  <img class="more-arrow" src="/static/index/u30.png"/>
                </div>
              </div>
              <div class="rankpic">
                <img src="/static/index/u38.png" class="first"/>
                <img src="/static/index/u39.png" class="second"/>
                <img src="/static/index/u40.png" class="third"/>
              </div>
              <div class="recommend-bookrank">
                <BookCard/>
                <BookCard/>
                <BookCard/>
              </div>
              <div class="booklist">
                <img src="/static/index/u46.png" class="booklistpic">
                <div class="booklist-text">书单推荐</div>
                <div class="more">
                  <div class="more-text">更多</div>
                  <img class="more-arrow" src="/static/index/u30.png"/>
                </div>
              </div>
              <div class="listbutton">
                <button class="firstlist">书单1号</button>
                <button class="secondlist">书单2号</button>
              </div>
            </div>
          </div>
        </div>
        <div class="saying">
          <div class="saying-head">
            <div class="saying-text">每日积累</div>
          </div>
          <div class="saying-content">
            <img src="/static/index/u87.png" class="saying-content-image">
            <div class="saying-content-text">天下兴亡，匹夫有责</div>
            <div class="saying-content-author">顾炎武</div>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom">
      <Bottom/>
    </div>
  </div>
</template>

<script>
import BookCard from '../../components/home/bookcard'
import Banner from '../../components/home/banner'
import Bottom from '../../components/home/bottom'
export default {
  components: {
    BookCard,
    Banner,
    Bottom
  },
  methods: {
    onMyClick () {
      this.$router.push('/pages/my/main')
    },
    onMessageClick () {
      this.$router.push('/pages/message/main')
    }
  }
}
</script>

<style scoped>
.head {
  border-width:0px;
  position:absolute;
  left:0px;
  top:0px;
  width:100%;
  height:45px;
}
.head-wrapper{
  padding: 10px 20px 10px 20px;
  display: flex;
}
.user{
  width: 30px;
  height: 30px;
}
.message{
  width: 30px;
  height: 30px;
}
.head-text{
  margin: 0 123px 0 123px;
  justify-content: center;
  align-items: center;
  font-size: 17px;
}
.content {
  position:absolute;
  left:0px;
  top:45px;
  width:100%;
  padding-bottom: 50px;
  background:inherit;
  background-color:rgba(234, 234, 234, 1);
  box-sizing:border-box;
  margin-bottom: 45px;
}
.content-wrapper{
  margin: 20px 20px 0 20px;
}
.library-head{
  margin: 20px 100px 0 100px;
  padding-top: 10px;
  height:72px;
  background-color: #A0D1E7;
  border-radius: 15px;
  justify-content: center;
  align-items: center;
}
.library-text{
  color:#13a3e6;
  margin-left: 40px;
}
.library-content{
  margin-top: -40px;
  padding: 20px 30px 10px 30px;
  height: 220px;
  background-color: #fff;
  border-radius: 15px;
}
.library-content-head{
  display: flex;
}
.allbooks {
  display: flex;
  padding: 5px 0 5px 17px;
  color: #13a3e6;
  background-color: #A0D1E7;
  border-radius: 10px;
  width: 120px;
  height: 30px;
  line-height: 20px;
  text-align: center;
  font-size: 17px;
}
.allbooks-text{
  margin: 5px 0 0 8px;
  color: #13a3e6;
  font-size: 17px;
}
.bookpic{
  margin-top: 7px;
  width: 18px;
  height: 18px;
}
.bookshelf{
  margin-left: 30px;
  display: flex;
  padding: 5px 0 5px 17px;
  color: #13a3e6;
  background-color: #A0D1E7;
  border-radius: 10px;
  width: 120px;
  height: 30px;
  line-height: 20px;
  text-align: center;
  font-size: 17px;
}
.bookshelf-text{
  margin: 5px 0 0 8px;
  color: #13a3e6;
  font-size: 17px;
}
.shelfpic{
  margin-top: 7px;
  width: 19px;
  height: 19px;
}
.library-content-book{
  padding-top :19px ;
  display: flex;
}
.recommend-head{
  margin: 20px 100px 0 100px;
  padding-top: 10px;
  height:72px;
  background-color: #e7a0c9dc;
  border-radius: 15px;
  justify-content: center;
  align-items: center;
}
.recommend-text{
  color:#fff;
  text-align: center;
}
.recommend-content{
  margin-top: -40px;
  padding: 20px 30px 10px 30px;
  background-color: #fff;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
}
.bookrank{
  display: flex;
  height: 30px;
}
.bookrankpic{
  margin-right: 5px;
  width: 25px;
  height: 25px;
}
.bookrank-text{
  font-size: 16px;
  margin-right: 125px;
}
.more{
  display: flex;
  margin-left: 22px;
}
.more-text{
  font-size: 16px;
}
.more-arrow{
  margin: 3px 0 0 5px;
  width: 10px;
  height: 20px;
}
.recommend-bookrank{
  padding-top :15px ;
  display: flex;
}
.rankpic{
  position: absolute;
  top: 545px;
  display: flex;
  z-index: 1;
}
.first{
  margin-right: 62px;
  width: 37px;
  height: 37px;
}
.second{
  margin-right: 62px;
  width: 37px;
  height: 37px;
}
.third{
  width: 37px;
  height: 37px;
}
.booklist{
  margin-top: 25px;
  display: flex;
  height: 30px;
}
.booklistpic{
  margin-right: 5px;
  width: 25px;
  height: 25px;
}
.booklist-text{
  font-size: 16px;
  margin-right: 107px;
}
.firstlist{
  margin-top: 15px;
  background-color: #fff;
  border-radius: 10px;
  border: 0.3px solid black;
  height: 40px;
  font-size: 16px;
  line-height: 40px;
  text-align: center;
}
.secondlist{
  margin-top: 12px;
  background-color: #fff;
  border-radius: 10px;
  border: 0.3px solid black;
  height: 40px;
  font-size: 16px;
  line-height: 40px;
  text-align: center;
  margin-bottom: 20px;
}
.saying-head{
  margin: 20px 100px 0 100px;
  padding-top: 10px;
  height:72px;
  background-color:black;
  border-radius: 15px;
  justify-content: center;
  align-items: center;
}
.saying-text{
  color:#fff;
  text-align: center;
}
.saying-content-image{
  margin-top: -40px;
  width: 100%;
  height:100px;
}
.saying-content-text{
  margin-top: -80px;
  color: #fff;
  font-size: 18px;
  height: 25px;
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
}
.saying-content-author{
  margin-top: 10px;
  color: #fff;
  font-size: 16px;
  height: 20px;
  margin-left: 250px;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
 