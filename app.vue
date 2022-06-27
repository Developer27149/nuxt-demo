<template>
  <div class="hello">
    <vue-ueditor-wrap
      ref="ueditor"
      v-model="msg"
      :destroy="false"
      :config="config"
      style="width: 600px; margin: 0 auto"
    ></vue-ueditor-wrap>
    <button @click="showData" class="preview">保存内容</button>
  </div>
</template>

<script>
import VueUeditorWrap from "vue-ueditor-wrap"; // ES6 Module
export default {
  components: {
    VueUeditorWrap,
  },
  data() {
    return {
      msg: "请输入内容",
      config: {
        // 编辑器不自动被内容撑高
        autoHeightEnabled: true,
        // 初始容器高度
        initialFrameHeight: 240,
        elementPathEnabled: false,
        wordCount: false,
        enableAutoSave: false,
        // 初始容器宽度
        initialFrameWidth: "100%",
        serverUrl: "",
      },
    };
  },
  methods: {
    showData() {
      console.log(this.msg);
    },
  },
};
</script>
