<template>
  <div class="his_container">
    <div class="history">
      <label class="el-icon-time film"></label>
      <h4 class="his_title" style="margin-left: 20px;">历史记录</h4>
    </div>
    <el-timeline>
      <el-timeline-item timestamp="2020/11/20" placement="top">
        <el-card>
          <div style="display: flex; flex-direction: row;">
            <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="his_img"/>
            <div class="his_text">
              <h4 class="his_title">这是标题</h4>
              <p class="his_desc">这是内容</p>
            </div>
          </div>
        </el-card>
      </el-timeline-item>
      <el-timeline-item timestamp="2020/11/20" placement="top">
        <el-card>
          <div style="display: flex; flex-direction: row;">
            <img src="../static/87fe289d6b49da542fbd8b6a152cd39c34034936.jpg@518w_1e_1c.jpg" class="his_img"/>
            <div class="his_text">
              <h4 class="his_title">这是标题</h4>
              <p class="his_desc">这是内容</p>
            </div>
          </div>
        </el-card>
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script>
</script>

<style>
  .his_container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    margin: 0 150px 0 120px;
  }

  .his_img{
    width: 198px;
    height: 120px;
  }

  .his_title{
    font-size: 28px;
    font-style: oblique;
    font-weight: 500;
  }

  .his_desc{
    font-size: 20px;
    color: #7F828B;
    margin-top: 50px;
  }

  .his_text{
    margin-left: 60px;
    height: 120px;
  }

  .history{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
  }
</style>
