<!-- 顶部组件 -->
<template>
  <div class="v-header-area">
    <router-link :to="{ path: '/' }" class="v-header-logo-area" title="首页">
      <div>
        <img src="../../common/img/logo.png" />
      </div>
      <span>X-Admin后台管理系统</span>
    </router-link>

    <el-menu
      default-active="1"
      mode="horizontal"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b" style="float: right;">
      <el-submenu index="1">
        <template slot="title">
          <img src="../../common/img/avatar.png" class="v-avatar-area" />
          <span>管理员</span>
        </template>
        <el-menu-item index="3-1">修改信息</el-menu-item>
        <el-menu-item index="3-2">退出登录</el-menu-item>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script type="text/ecmascript-6">
  const COMPONENT_NAME = 'v_header';

  export default {
    name: COMPONENT_NAME,
    data() {
      return {

      }
    },
    methods: {}
  }
</script>

<style scoped lang="less" type="text/less" rel="stylesheet/less">
  @import "../../common/styles/index";

  .v-header-area {
    display: flex;
    justify-content: space-between;
    background-color: @background-color;
    height: @header-height;
    .v-header-logo-area {
      display: flex;
      justify-content: center;
      align-items: center;
      box-sizing: border-box;
      padding: 0 25px 0 10px;
      text-decoration: none;
      div {
        font-size: 0;
        display: block;
        img {
          display: block;
          width: @header-height - 5px;
          height: @header-height - 10px;
        }
      }
      span {
        color: #fff;
        font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
      }
      &:hover {
        background-color: @active-background-color;
      }
    }
  }

  .v-avatar-area {
    display: inline-block;
    width: @header-height - 10px;
    height: @header-height - 10px;
  }
</style>
