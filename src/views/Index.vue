<template>
  <div>
    <!-- 轮播图 -->
    <div class="runImage">
      <el-carousel height="450px">
        <el-carousel-item v-for="(v,k) in carousel" :key="k">
          <img :src="v" alt width="100%" height="100%">
        </el-carousel-item>
      </el-carousel>
    </div>
    <!-- 电影列表 left -->
    <div class="movie-main">
      <el-row :gutter="30">
        <!-- 左 -->
        <el-col :span="18">
          <!-- 第二层 -->
          <div class="movie-info">
            <el-row :gutter="30">
                <!-- <el-col class="card-info" :span="8" v-for="(v,k) in movies" :key="k" style=" margin-bottom: 10px; ">
                    <el-card class="card-item" :body-style="{ padding: '0px' }">
                      <img :src="v.img" class="card-img">
                      <div style="padding: 14px;" class="span-info">
                        <span>译  名：{{v.translate}}</span>
                        <span>片  名：{{v.title}}</span>
                        <span>年  代：{{v.years}}</span>
                        <span>产  地：{{v.home}}</span>
                        <span>类  别：{{v.type}}</span>
                      </div>
                    </el-card>
                </el-col> -->
                <div class="masonry"> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/4047.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                    <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/5241.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/0155.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/5620.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/0112.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/6029.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/6029.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/0112.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                  <div class="item"> 
                    <div class="item__content">
                      <img src="../assets/5620.jpg" alt="">
                      <div class="span-info">
                        <span>译  名：Hidden Man / 侠隐</span>
                        <span>片  名：邪不压正</span>
                        <span>年  代：2018</span>
                        <span>产  地：中国大陆</span>
                        <span>类  别：剧情 / 喜剧 / 动作</span>
                      </div>
                    </div> 
                  </div> 
                </div>
            </el-row>
            <!-- 第二层END -->
          </div>
        </el-col>
        <!-- 右 -->
        <el-col :span="6">
          <div class="ranking_list">
              <el-tabs type="border-card">
              <el-tab-pane label="最新发布">
                <ul>
                  <li v-for="(v,k) in ranking.new" :key="k" :class="{danger:k<3,info:k>=3}">{{k+1}}、{{v}}</li>
                </ul>
              </el-tab-pane>
              <el-tab-pane label="推荐">
                <ul>
                  <li v-for="(v,k) in ranking.recommend" :key="k" :class="{danger:k<3,info:k>=3}">{{k+1}}、{{v}}</li>
                </ul>
              </el-tab-pane>
              <el-tab-pane label="点击最多">
                <ul>
                  <li v-for="(v,k) in ranking.most" :key="k" :class="{danger:k<3,info:k>=3}">{{k+1}}、{{v}}</li>
                </ul>
              </el-tab-pane>
              <el-tab-pane label="好评最多">
                <ul>
                  <li v-for="(v,k) in ranking.like" :key="k" :class="{danger:k<3,info:k>=3}">{{k+1}}、{{v}}</li>
                </ul>
              </el-tab-pane>
            </el-tabs>
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeName2: 'first',
      carousel: [
        require("../assets/5eee188505d29c7cf7417eaab3f6120d.jpg"),
        require("../assets/6a41ed57bc768a0a88102ebca00e2d7b.jpg"),
        require("../assets/f4e899356fae83445854de54935e7f94.jpg"),
        require("../assets/a449d6fb9333d70f266b4c7463dc287f.jpg")
      ],
      ranking: {
        new:[
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
          "冰海陷落/潜舰猎杀令(台)/猎人杀手",
        ],
        recommend:[
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
          "漫画少年的遐想世界/KillsonWheels",
        ],
        most:[
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
          "Detective Dee",
        ],
        like:[
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
          "功夫大联盟/Kung Fu League",
        ], 
      },
      movies:[
        {
          'img': require("../assets/carousel11.jpg"),
          'translate':"Hidden Man / 侠隐",
          'title':"邪不压正",
          'years':"2018",
          'home':"中国大陆",
          'type':"剧情 / 喜剧 / 动作"
        },
        {
          'img': require("../assets/carousel33.jpg"),
          'translate':"Hidden Man / 侠隐",
          'title':"邪不压正",
          'years':"2018",
          'home':"中国大陆",
          'type':"剧情 / 喜剧 / 动作"
        },
        {
          'img': require("../assets/carousel44.jpg"),
          'translate':"Hidden Man / 侠隐",
          'title':"邪不压正",
          'years':"2018",
          'home':"中国大陆",
          'type':"剧情 / 喜剧 / 动作"
        },
        {
          'img': require("../assets/carousel44.jpg"),
          'translate':"Hidden Man / 侠隐",
          'title':"邪不压正",
          'years':"2018",
          'home':"中国大陆",
          'type':"剧情 / 喜剧 / 动作"
        },
        {
          'img': require("../assets/carousel44.jpg"),
          'translate':"Hidden Man / 侠隐",
          'title':"邪不压正",
          'years':"2018",
          'home':"中国大陆",
          'type':"剧情 / 喜剧 / 动作"
        },
        {
          'img': require("../assets/carousel44.jpg"),
          'translate':"Hidden Man / 侠隐",
          'title':"邪不压正",
          'years':"2018",
          'home':"中国大陆",
          'type':"剧情 / 喜剧 / 动作"
        }
      ]
    };
  },
  created:function(){
    
  },
  methods: {

  }
};
</script>

<style scoped>
.runImage{
  padding: 0 190px;
}
/* 首页内容主题 */
.movie-main {
  margin-top: 20px;
  padding: 0 190px;
}
/* 信息卡片 */
.movie-info{
  overflow:hidden;
  padding-left: 20px;
  margin-left: -5px;
}
.movie-info img{
  width: 100%;
  display: block;
}
.span-info span{
  display: block;
  overflow: hidden; 
  text-overflow: ellipsis; 
  -o-text-overflow: ellipsis;
  white-space:nowrap;
}
/* 排行榜 */
.ranking_list li{
  width: 100%;
  line-height: 1.5em;
  padding: 5px 0;
  text-indent: 0.8em;
  border-bottom: 1px solid #f3f3f3;
  /* color: #F56C6C; */
}
.info{
  color: #909399;
}
.danger{
  color: #F56C6C;
}
</style>
