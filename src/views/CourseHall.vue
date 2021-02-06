<template>
  <div class="course-hall">
    <div class="course-tab">
      <div class="tab-left"></div>
      <div class="tab-right">
        <div class="region">
          <p class="name">地区：</p>
          <div class="r-data">
            <div
              v-for="(item, index) in regionData"
              :key="index"
              :class="regionIndex === index ? 'active' : ''"
              @click="regionClick(index)"
            >
              {{ item.value }}
            </div>
          </div>
        </div>
        <div class="major">
          <p class="name">专业：</p>
          <div class="r-data">
            <div
              v-for="(item, index) in majorData"
              :key="index"
              :class="majorIndex === index ? 'active' : ''"
              @click="majorClick(index)"
            >
              {{ item.value }}
            </div>
          </div>
        </div>
        <div class="group">
          <div class="name">群体：</div>
          <div class="r-data">
            <div
              v-for="(item, index) in groupData"
              :key="index"
              :class="groupIndex === index ? 'active' : ''"
              @click="groupClick(index)"
            >
              {{ item.value }}
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="course-content">
      <div class="content-item">
        <div class="left"></div>
        <div class="right">
          <div class="title">标题标题标题标题</div>
          <div class="describe">
            描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述
          </div>
        </div>
      </div>
      <div class="content-item">
        <div class="left"></div>
        <div class="right">
          <div class="title">标题标题标题标题</div>
          <div class="describe">
            描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述
          </div>
        </div>
      </div>
      <div class="content-item">
        <div class="left"></div>
        <div class="right">
          <div class="title">标题标题标题标题</div>
          <div class="describe">
            描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      regionIndex: 0,
      majorIndex: 0,
      groupIndex: 0,
      regionData: [
        {
          value: "天津",
        },
        {
          value: "北京",
        },
        {
          value: "河北",
        },
      ],
      majorData: [
        {
          value: "自主研发",
        },
        {
          value: "模具开发",
        },
        {
          value: "精雕",
        },
        {
          value: "语言",
        },
      ],
      groupData: [
        {
          value: "社区",
        },
        {
          value: "企业职工",
        },
        {
          value: "牧师",
        },
        {
          value: "学生",
        },
        {
          value: "党政管理人员",
        },
        {
          value: "进城务工人员",
        },
        {
          value: "农村劳动者",
        },
        {
          value: "社区老年人",
        },
      ],
    };
  },
  methods: {
    regionClick(i) {
      this.regionIndex = i;
    },
    majorClick(i) {
      this.majorIndex = i;
    },
    groupClick(i) {
      this.groupIndex = i;
    },
  },
};
</script>

<style lang="scss" scoped>
.course-hall {
  background-color: #f0f2f5;
  overflow: hidden;
  padding-bottom: 50px;
  .course-tab {
    margin-top: 35px;
    display: flex;
    height: 200px;
    background-color: #fff;
    .tab-left {
      width: 12px;
      height: 100%;
      background-color: #00b486;
      border-radius: 6px;
    }
    .tab-right {
      flex: 1;
      padding: 0 60px;
      .region,
      .major,
      .group {
        display: flex;
        margin-top: 24px;
        &.region {
          margin-top: 50px;
        }
        .name {
          font-size: 14px;
          font-weight: 800;
        }
        .r-data {
          display: flex;
          div {
            line-height: 20px;
            text-align: center;
            padding: 0 16px;
            border-radius: 4px;
            color: #fbfbfb;
            background-color: #cccccc;
            margin-left: 15px;
            cursor: pointer;
            &.active {
              background-color: #00b486;
              color: #fff;
            }
          }
        }
      }
    }
  }
  .course-content {
    .content-item {
      margin-top: 35px;
      display: flex;
      padding: 20px;
      background-color: #fff;
      .left {
        height: 160px;
        width: 250px;
        background-color: #00b486;
        border-radius: 4px;
      }
      .right {
        margin-left: 30px;
        .title {
          font-size: 18px;
          line-height: 40px;
        }
        .describe {
          font-size: 12px;
          color: #4b4b4b;
          line-height: 1.5;
        }
      }
    }
  }
}
</style>
