<template>
  <div class="container">
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
          <h1 class="title" style="margin-left: 6.25rem;">
            消息
          </h1>
        </div>
        <div v-on:mouseenter="visible" @mouseleave="invisible" class="hint">
          <div class="hint_1">
            <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="face"></img>
            <p v-show="seen">点击进入个人主页</p>
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
  margin-left: 190px;
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

</style>
