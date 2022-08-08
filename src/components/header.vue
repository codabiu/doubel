<template>
  <div class="header">
    <el-menu
      :default-active="this.$route.path"
      router
      mode="horizontal"
      background-color="#fff"
      text-color="#303133"
      active-text-color="#409EFF"
    >
      <el-menu-item v-for="(item,i) in navList" :key="i" :index="item.name" :class="item.class">
        {{ item.navItem }}
      </el-menu-item>
    </el-menu>
  </div>
</template>
<script>
export default {
  data () {
    return {
      navList: [
        {name: '', class: 'name', navItem: 'double'},
        {name: '/', class: 'index', navItem: '首页'},
        {name: '/blog', class: 'blog', navItem: '博客文章'},
        {name: '/schedule', class: 'schedule', navItem: '待办事项'},
        {name: '/about_me', class: 'about_me', navItem: '关于我'},
        {name: '/message', class: 'message', navItem: '留言板'}
      ]
    }
  },
  methods: {
  }
}
</script>

<style lang="less" scoped>
  .header {
    // position: fixed;
    // z-index: 3;
    // width: 100%;
  }
  .name {
    font-size: 18px;
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  }
  .index,.blog, .schedule, .aboutMe, .message{
    font-size: 15px;
  }
  .index{
      margin-left: 5%
  }
</style>
