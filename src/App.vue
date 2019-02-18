<template>
  <el-container>
    <!-- 头部部分 -->
    <el-header>
      <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        background-color="#303133"
        text-color="#fff"
        :router="true"
        active-text-color="#ffd04b"
      >
        <el-menu-item index="1">首页</el-menu-item>
        <el-menu-item index="2" >最新50部</el-menu-item>
        <el-menu-item index="3" >动漫</el-menu-item>
        <el-menu-item index="4" >喜剧片</el-menu-item>
        <el-menu-item index="5" >动作片</el-menu-item>
        <el-menu-item index="6" >爱情片</el-menu-item>
        <el-menu-item index="7" >恐怖片</el-menu-item>
        <el-menu-item index="8" >剧情片</el-menu-item>
        <el-menu-item index="9" >战争片</el-menu-item>
        <el-menu-item index="10">纪录片</el-menu-item>
        <el-menu-item index="11">电视剧</el-menu-item>
        <el-menu-item index="12">综艺</el-menu-item>
      </el-menu>
    </el-header>
    <!-- 主体部分 -->
    <el-main>
      <router-view></router-view>
    </el-main>
  </el-container>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

<style scoped>
.el-menu-item {
  padding: 0 26px;
}

</style>
