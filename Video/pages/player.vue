<template>
  <div class="container">
    <div class="pla_head">
      <div class="column">
        <div class="row">
          <label class="pla_label">娱乐</label>
          <h4 class="pla_titile" style="margin-left: 24px;">这是标题这是标题</h4>
        </div>
        <div class="video-player-box" :playsinline="playsinline" v-video-player:myVideoPlayer="playerOptions"></div>
        <div class="pla_text">
          <p class="pla_desc">这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述这是描述</p>
        </div>
      </div>
      <div class="column" style="margin-left: 98px;">
        <div class="row">
          <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="pla_face" style="margin-top: 36px;"></img>
          <h4 class="pla_name"> 用户1</h4>
        </div>
        <button class="pla_care">点击关注</button>
        <div :class="[isClick?'pla_triplet_1':'pla_triplet']" @click="changeColor">
          <label class="el-icon-star-off pla_icon"></label>
          <h4 class="pla_number">1234</h4>
        </div>
        <div class="pla_triplet">
          <label class="el-icon-share pla_icon"></label>
          <h4 class="pla_number">1234</h4>
        </div>
        <div class="pla_triplet">
          <label class="el-icon-download pla_icon"></label>
          <h4 class="pla_number">1234</h4>
        </div>
        <label class="pla_topic" style="height: 36px; margin-top: 36px;">#话题1</label>
        <label class="pla_topic" style="height: 36px; margin-top: 18px;">#话题2</label>
        <label class="pla_topic" style="height: 36px; margin-top: 18px;">#话题3</label>
      </div>
    </div>
    <div class="pla_line"></div>
    <h4 class="pla_titile" style="margin: 0px 198px 36px 198px;">评论</h4>
    <div class="pla_mid">
      <div class="row">
        <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="pla_face"></img>
        <form>
          <input type="text" value="发表评论" maxlength="250" class="pla_meseage"/>
        </form>
        <button class="pla_send">发表评论</button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
      data () {
        return {
          playsinline: true,
          playerOptions: {//播放器配置
          muted: false,//是否静音
          language: 'zh-CN',
          preload: 'auto', //视频预加载
          autoplay: false,
          //aspectRatio: '16:9',
          controls: true,
          width:'600px',
          height:'400px',
          loop: false,//一结束重新开始
          playbackRates: [0.7, 1.0, 1.5, 2.0],//播放速度
          sources: [{
            type: "video/mp4",
            src: "https://cdn.theguardian.tv/webM/2015/07/20/150716YesMen_synd_768k_vp8.webm"
          }],
          poster: "",//封面图
          notSupportedMessage: '此视频暂无法播放，请稍后再试',
          isClick:false
          }
        }
      },
      methods: {
        changeColor: function(){
          this.isClick=!this.isClick;
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

  .pla_head{
    margin: 36px 216px 36px 216px;
    display: flex;
    flex-direction: row;
  }

  .pla_mid{
    margin: 0px 216px 36px 216px;
    display: flex;
    flex-direction: row;
  }

  .row{
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .column{
    display: flex;
    flex-direction: column;
  }

  .video-player-box{
    margin-top: 18px;
    width: 600px;
    height: 400px;
  }
  /* 播放按钮居中 */
  .video-js .vjs-big-play-button{
      font-size: 2.5em;
      line-height: 2.3em;
      height: 2.5em;
      width: 2.5em;
      border-radius: 2.5em;
      background-color: #73859f;
      background-color: rgba(115,133,159,.5);
      border-width: 0.15em;
      margin-left: 260px;
      margin-top: 160px;
  }
  /* 中间的播放箭头 */
  .vjs-big-play-button .vjs-icon-placeholder {
      font-size: 1.63em;
  }

  .pla_titile{
    font-size: 28px;
    font-weight: 500;
  }

  .pla_label{
    font-size: 20px;
    font-weight: 500;
    padding: 6px 18px 6px 18px;
    color: #FFFFFF;
    border: 1px solid #00aaff;
    border-radius: calc(6px);
    background-color: #00AAFF;
  }

  .pla_desc{
    font-size: 14px;
    color: #000000;
  }

  .pla_text{
    margin-top: 18px;
    width: 600px;
    padding: 0 18px 0 18px;
  }

  .pla_face{
    width: 54px;
    height: 54px;
    border:1px solid blueviolet;
    border-radius: 54px;
  }

  .pla_name{
    font-size: 20px;
    font-weight: 500;
    margin-left: 36px;
  }

  .pla_care{
    margin-top: 18px;
    background-color:#0055ff;
    width: 198px;
    height: 36px;
    font-size:14px;
    color: #FFFFFF;
    padding:initial;
    border-radius: 0.3125rem;
    border: #aa00ff;
  }

  .pla_icon{
    font-size: 36px;
  }

  .pla_triplet{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 36px;
    color: #55aaff;
  }

  .pla_triplet_1{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 36px;
    color: #ff0000;
  }

  .pla_number{
    font-size: 18px;
    margin-left: 6px;
  }

  .pla_topic{
    margin-top: 18px;
    background-color:#55ffff;
    width: 198px;
    height: 50%;
    font-size:14px;
    color: #000000;
    padding:initial;
    border-radius: 36px;
    border: #aa00ff;
    text-align: center;
  }
/* 伪元素垂直居中 */
  .pla_topic::before{
    display: inline-block;
    content: "";
    height: 100%;
    vertical-align: middle;
  }

  .pla_line{
    border: 1px solid #000000;
    margin: 0px 198px 36px 198px;
  }

  .pla_meseage{
    margin-left: 36px;
    width: 648px;
    height: 56px;
  }

  .pla_send{
    background-color:#ff0000;
    width: 98px;
    height: 56px;
    font-size:16px;
    color: #FFFFFF;
    padding:initial;
    border-radius: 0.3125rem;
    border: #ff5500;
    margin-left: 36px;
  }
</style>
