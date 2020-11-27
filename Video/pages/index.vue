<template>
  <div class="container">
    <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css">
    <!-- 标签栏-->
    <div class="head">
      <div class="head_1">
        <div style="display: flex; flex-direction: row;">
          <h1 class="title" @click="reload">
            主页
          </h1>
          <h1 class="title" style="margin-left: 6.25rem;" @click="history">
            历史
          </h1>
          <h1 class="title" style="margin-left: 6.25rem;" @click="message">
            消息
          </h1>
        </div>
        <div class="hint">
          <div class="hint_1">
            <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="face"
            @click="myPage"></img>
          </div>
        </div>
        <div style="margin-left: 80px;">
          <form>
            <input type="text" size="12" value="搜索" maxlength="250" class="select"/>
          </form>
        </div>
        <div style="margin-left: 100px;">
          <button type="button" class="send" formaction="https://www.bilibili.com/">投稿</button>
        </div>
      </div>
    </div>

    <div style="border: 1px solid #8A2BE2;"></div>

    <!-- 图标栏-->
    <div class="icon">
      <div class="icon_1">
        <label class="el-icon-film film" @click="player"></label>
        <p>影视</p>
      </div>
      <div class="icon_1">
        <label class="el-icon-magic-stick film"></label>
        <p>娱乐</p>
      </div>
      <div class="icon_1">
        <label class="el-icon-suitcase film"></label>
        <p>生活</p>
      </div>
      <div class="icon_1">
        <label class="el-icon-lollipop film"></label>
        <p>动画</p>
      </div>
      <div class="icon_1">
        <label class="el-icon-headset film"></label>
        <p>音乐</p>
      </div>
    </div>

    <div style="display: flex; flex-direction: row; margin-top: 18px;">
      <!-- 轮播图-->
    <div class="image">
      <el-carousel :interval="5000"height="400px" autoplay=true>
          <el-carousel-item v-for="item in 4" :key="item">
            <h3>{{ item }}</h3>
          </el-carousel-item>
      </el-carousel>
    </div>


      <!-- 列表-->
      <div class="list">
        <h1 class="title">
          排行榜
        </h1>
        <div class="list_1">
          <p>这是内容</p>
          <div style="border: 1px solid #55ffff; margin-top: 10px;"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      seen:false
    }
  },
  methods:{
    history: function(){
      this.$router.push('history');
    },
    myPage: function(){
      this.$router.push('myPage');
    },
    message: function(){
      this.$router.push('message');
    },
    player: function(){
      this.$router.push('player');
    },
    reload:function(){
      location.reload();
    },
    visible:function(){
      this.seen = true;
    },
    invisible:function(){
      this.seen = false;
    }
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  /* justify-content: center; 水平居中 */
  /* align-items: center; 垂直居中 */
}

.head{
  padding: 10px;
  z-index: 1;
  background-image: url(../static/3f3371d2ca100511e0b5e3373fd269c8.png);
}

.head_1{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.title {
  display: inline;
  font-weight: 300;
  font-size: 27px;
  color: #35495e;
  letter-spacing: 1px;
  z-index: 1;
}

.face{
  width: 54px;
  height: 54px;
  border:1px solid blueviolet;
  border-radius: 54px;
}

.hint{
  margin-left: 198px;
  justify-content: center;
  align-items: center;
  width: 130px;
}

.hint_1{
  justify-content: center;
  align-items: center;
}

.send{
  background-color:#ff0000;
  width: 4.5rem;
  height: 2.25rem;
  font-size: 1.25rem;
  color: #FFFFFF;
  padding:initial;
  border-radius: 0.3125rem;
  border: #FF5500;
  z-index: 1;
}

.select{
  width: 256px;
  height: 27px;
  z-index: 1;
}

.film{
  font-size: 45px;
  color: #ff5500;
}

.icon{
  padding: 20px;
  display: flex;
  flex-direction: row;
}

.icon_1{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-left: 180px;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(n) {
   background-image: url(../static/75941497_0.png);
   background-size: 100% 100%;
}

.image{
  width: 600px;
  height: 400px;
  margin-left: 98px;
}

.ima{
  margin: 0 70px 0 70px;
}

.list{
  width: 500px;
  height: 400px;
  margin-left: 50px;
}

.list_1{
  margin-top: 20px;
  width: 500px;
  height: 300px;
  border:1px solid blueviolet;
  padding: 10px;
}

</style>
