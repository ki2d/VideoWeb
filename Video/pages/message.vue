<template>
  <div class="container">
    <el-tabs v-model="activeName" @tab-click="handleClick" tab-position="top" stretch="true">
      <el-tab-pane label="粉丝" name="first">
        <el-timeline class="mes_container">
          <el-timeline-item timestamp="2020/11/20" placement="top">
            <el-card>
              <div class="mes_card">
                <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mes_face"></img>
                <div class="mes_text">
                  <h4 class="mes_name">程序员</h4>
                  <p class="mes_notice">关注了你</p>
                </div>
                <button type="button" class="replay">回关</button>
              </div>
            </el-card>
          </el-timeline-item>
          <el-timeline-item timestamp="2020/11/20" placement="top">
            <el-card>
              <div class="mes_card">
                <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mes_face"></img>
                <div class="mes_text">
                  <h4 class="mes_name">程序员</h4>
                  <p class="mes_notice">关注了你</p>
                </div>
                <button type="button" class="replay">回关</button>
              </div>
            </el-card>
          </el-timeline-item>
        </el-timeline>
      </el-tab-pane>
      <el-tab-pane label="点赞" mes_name="second">
        <el-timeline class="mes_container">
          <el-timeline-item timestamp="2020/11/20" placement="top">
            <el-card>
              <div class="mes_card">
                <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mes_face"></img>
                <div class="mes_text">
                  <h4 class="mes_name">程序员...</h4>
                  <p class="mes_notice">等共9人赞了你的作品</p>
                </div>
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mes_img"/>
              </div>
            </el-card>
          </el-timeline-item>
          <el-timeline-item timestamp="2020/11/20" placement="top">
            <el-card>
              <div class="mes_card">
                <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mes_face"></img>
                <div class="mes_text">
                  <h4 class="mes_name">程序员...</h4>
                  <p class="mes_notice">等共9人赞了你的作品</p>
                </div>
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mes_img"/>
              </div>
            </el-card>
          </el-timeline-item>
        </el-timeline>
      </el-tab-pane>
      <el-tab-pane label="评论" mes_name="third">
        <el-timeline class="mes_container">
          <el-timeline-item timestamp="2020/11/20" placement="top">
            <el-card>
              <div class="mes_card">
                <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mes_face"></img>
                <div class="mes_text">
                  <div style="display: flex; flex-direction: row;">
                    <h4 class="mes_name">程序员</h4>
                    <p class="mes_notice" style="margin-left: 18px;">评论了你的作品</p>
                  </div>
                  <p class="mes_notice">这是评论这是评论这是评论</p>
                  <button type="button" class="replay_1">回复</button>
                  <button type="button" class="like" style="margin-left: 36px;">点赞</button>
                </div>
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mes_img"/>
              </div>
            </el-card>
          </el-timeline-item>
          <el-timeline-item timestamp="2020/11/20" placement="top">
            <el-card>
              <div class="mes_card">
                <img src="../static/9c48806ed8b95d160bb75b076d5f370d.jpg" alt="头像" class="mes_face"></img>
                <div class="mes_text">
                  <div style="display: flex; flex-direction: row;">
                    <h4 class="mes_name">程序员</h4>
                    <p class="mes_notice" style="margin-left: 18px;">评论了你的作品</p>
                  </div>
                  <p class="mes_notice">这是评论这是评论这是评论</p>
                  <button type="button" class="replay_1">回复</button>
                  <button type="button" class="like" style="margin-left: 36px;">点赞</button>
                </div>
                <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="mes_img"/>
              </div>
            </el-card>
          </el-timeline-item>
        </el-timeline>
      </el-tab-pane>
    </el-tabs>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        activeName: 'first'
      };
    },
    methods:{
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>

<style>
  .mes_container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    margin: 0 150px 0 120px;
  }

  .mes_face{
    width: 54px;
    height: 54px;
    border:1px solid blueviolet;
    border-radius: 54px;
  }

  .mes_card{
    margin-left: 54px;
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .mes_name{
    font-size: 20px;
    font-style: oblique;
    font-weight: 500;
  }

  .mes_notice{
    font-size: 16px;
    color: #7F828B;
  }

  .mes_text{
    margin-left: 54px;
    line-height:calc(30px);
    width: 360px;
  }

  .replay{
    background-color:#ff0000;
    width: 4.5rem;
    height: 2.25rem;
    font-size: 1.25rem;
    color: #FFFFFF;
    padding:initial;
    border-radius: 0.3125rem;
    border: #FF5500;
    margin-left: 54px;
  }

  .like{
    background-color:#00aaff;
    width: 72px;
    height: 24px;
    font-size:14px;
    color: #FFFFFF;
    padding:initial;
    border-radius: 0.3125rem;
    border: #55ffff;
  }

  .replay_1{
    background-color:#ffffff;
    width: 72px;
    height: 24px;
    font-size:14px;
    color: #00aaff;
    padding:initial;
    border-radius: 0.3125rem;
    border:1px solid #00aaff;
  }

  .mes_img{
    width: 162px;
    height: 108px;
    margin-left: 200px;
  }

</style>
