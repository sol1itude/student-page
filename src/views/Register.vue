<template>
  <div class="register">
    <h1 class="title">职教集团企业培训管理平台</h1>
    <div class="form-list">
      <div class="form-item" v-for="(item, index) in formData" :key="index">
        <p>{{ item.name }}：</p>
        <div v-if="item.type === 'input'">
          <input type="text" v-model="item.value" />
        </div>
        <div v-if="item.type === 'select'">
          <select v-model="item.value">
            <option
              v-for="(selectItem, selectIndex) in item.data"
              :key="selectIndex"
              :label="selectItem.label"
              :value="selectItem.value"
            ></option>
          </select>
        </div>
      </div>
    </div>
    <button class="btn">注册</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: [
        {
          name: "社会身份",
          value: "1",
          type: "select",
          data: [
            {
              label: "社区居民",
              value: "1",
            },
            {
              label: "居民",
              value: "2",
            },
          ],
        },
        {
          name: "姓名",
          value: "12",
          type: "input",
        },
        {
          name: "年龄",
          value: "12",
          type: "input",
        },
        {
          name: "从业年龄",
          value: "",
          type: "input",
        },
        {
          name: "专业",
          value: "",
          type: "input",
        },
        {
          name: "工作单位",
          value: "",
          type: "input",
        },
        {
          name: "岗位",
          value: "",
          type: "input",
        },
        {
          name: "行业",
          value: "",
          type: "input",
        },
        {
          name: "身份",
          value: "2",
          type: "select",
          data: [
            {
              label: "社区居民",
              value: "1",
            },
            {
              label: "居民",
              value: "2",
            },
          ],
        },
        {
          name: "证件号码",
          value: "",
          type: "input",
        },
        {
          name: "登陆用户名",
          value: "",
          type: "input",
        },
        {
          name: "登陆密码",
          value: "",
          type: "input",
        },
        {
          name: "确认登录密码",
          value: "",
          type: "input",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.register {
  overflow: hidden;
  h1.title {
    font-size: 34px;
    color: #00b486;
    margin-top: 100px;
    text-align: center;
  }
  .form-list {
    margin-top: 30px;
    .form-item {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 12px;
      p {
        width: 7em;
        text-align: right;
      }
      div {
        width: 295px;
        input,
        select {
          width: 100%;
          height: 24px;
          line-height: 24px;
          border: 1px solid #e2e2e2;
          padding: 0 10px;
        }
      }
    }
  }
  .btn {
    display: block;
    margin: 30px auto;
  }
}
</style>
