<template>
  <div class="mpa_container">
    <div class="mpa_head">
      <div class="mpa_head_1">
        <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mpa_face"></img>
        <div class="mpa_text">
          <h4 class="mpa_praise">昵称</h4>
          <p class="mpa_number">个性签名个性签名个性签名个性签名</p>
        </div>
        <div class="mpa_triplet" style="margin-left: 360px;">
          <h4 class="mpa_praise">获赞</h4>
          <p class="mpa_number">1234</p>
        </div>
        <div class="mpa_triplet">
          <h4 class="mpa_praise">粉丝</h4>
          <p class="mpa_number">1234</p>
        </div>
        <div class="mpa_triplet">
          <h4 class="mpa_praise">关注</h4>
          <p class="mpa_number">1234</p>
        </div>
      </div>
      <div class="mpa_body">
        <el-tabs v-model="activeName" @tab-click="handleClick" tab-position="top" stretch="true">
          <el-tab-pane label="喜欢" name="first">
            <div style="display: flex;flex-direction: row;">
              <div class="mpa_cover">
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mpa_img"/>
                <h4 class="mpa_praise">这是标题</h4>
              </div>
              <div class="mpa_cover">
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mpa_img"/>
                <h4 class="mpa_praise">这是标题</h4>
              </div>
              <div class="mpa_cover">
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mpa_img"/>
                <h4 class="mpa_praise">这是标题</h4>
              </div>
              <div class="mpa_cover">
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mpa_img"/>
                <h4 class="mpa_praise">这是标题</h4>
              </div>
              <div class="mpa_cover">
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mpa_img"/>
                <h4 class="mpa_praise">这是标题</h4>
              </div>
            </div>
          </el-tab-pane>
          <el-tab-pane label="作品" mes_name="second">
            <el-card>
              <div class="mpa_card">
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mpa_img"/>
                <div class="mpa_column">
                   <h4 class="mpa_title" style="margin-left: 54px;">这是标题</h4>
                   <div class="mpa_row">
                     <div class="mpa_triplet_1">
                       <label class="el-icon-video-play mpa_icon"></label>
                       <h4 class="mpa_number_1">1234</h4>
                     </div>
                     <div class="mpa_triplet_1">
                       <label class="el-icon-star-off mpa_icon"></label>
                       <h4 class="mpa_number_1">1234</h4>
                     </div>
                     <div class="mpa_triplet_1">
                       <label class="el-icon-time mpa_icon"></label>
                       <h4 class="mpa_number_1">2020.11.11</h4>
                     </div>
                   </div>
                </div>
              </div>
              
            </el-card>
          </el-tab-pane>
        </el-tabs>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        activeName: 'first'
      };
    },
  }
</script>

<style>
  .mpa_container{
    display: flex;
    flex-direction: column;
  }

  .mpa_row{
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 36px;
  }

  .mpa_column{
    display: flex;
    flex-direction: column;
  }

  .mpa_head{
    z-index: 1;
    width: 100%;
    height: 126px;
    padding: 36px 128px 36px 128px;
    background-image: url(../static/3f3371d2ca100511e0b5e3373fd269c8.png);
  }

  .mpa_head_1{
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .mpa_body{
    margin-top: 36px;
  }

  .mpa_face{
    width: 54px;
    height: 54px;
    border:1px solid blueviolet;
    border-radius: 54px;
  }

  .mpa_text{
    margin-left: 36px;
    line-height:calc(30px);
    width: 360px;
  }

  .mpa_triplet{
    margin-left: 36px;
    line-height:calc(30px);
    width: 54px;
  }

  .mpa_triplet_1{
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-left: 54px;
    width: 54px;
    color: #0055FF;
  }

  .mpa_praise{
    font-size: 18px;
  }

  .mpa_title{
    font-size: 24px;
  }

  .mpa_number{
    font-size: 14px;
    font-style: oblique;
  }

  .mpa_number_1{
    font-size: 16px;
    font-style: oblique;
    margin-left: 9px;
  }

  .mpa_img{
    width: 180px;
    height: 120px;
  }

  .mpa_cover{
    width: 180px;
    height: 170px;
    margin: 20px;
  }

  .mpa_card{
    margin-left: 36px;
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .mpa_icon{
    font-size: 28px;
  }
</style>
