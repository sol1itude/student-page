<template>
  <div class="header">
    <p class="name">企业培训管理平台</p>
    <div class="tab">
      <div
        class="tab-item"
        :class="active === index ? 'active' : ''"
        v-for="(item, index) in tab"
        :key="index"
        @click="tabClick(index)"
      >
        {{ item.name }}
      </div>
    </div>
    <div class="user">
      <div class="search">
        <input type="text" placeholder="单行输入" />
        <div>搜索</div>
      </div>
      <div class="user-name">Admin</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: 0,
      tab: [
        {
          name: "首页",
        },
        {
          name: "学习中心",
        },
        {
          name: "课程大厅",
        },
      ],
    };
  },
  methods: {
    tabClick(i) {
      this.active = i;
    },
  },
};
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 90px;
  background-color: #00b486;
  display: flex;
  align-items: center;
  padding: 0 30px;
  .name {
    font-size: 18px;
    color: #fff;
  }
  .tab {
    flex: 1;
    margin-left: 70px;
    display: flex;
    height: 100%;
    align-items: center;
    div.tab-item {
      color: #fff;
      height: 100%;
      line-height: 90px;
      font-size: 16px;
      width: 140px;
      text-align: center;
      cursor: pointer;
      user-select: none;
      &.active {
        background-color: #0b9e78;
      }
    }
  }
  .user {
    display: flex;
    div.search {
      display: flex;
      line-height: 20px;
      background-color: #32c7a2;
      input {
        width: 130px;
        border: none;
        outline: none;
        background-color: #32c7a2;
        color: #fff;
        padding-left: 20px;
      }
      div {
        width: 40px;
        background-color: #5adf96;
        text-align: center;
        color: #fff;
      }
    }
    .user-name {
      color: #fff;
      margin-left: 25px;
    }
  }
}
</style>
