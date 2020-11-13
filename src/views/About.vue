<template>
  <div class="a1">
    <div class="a3">
      <div class="a7"><button @click="fabiao" class="a6">发表</button></div>
      <div class="a9">
        <input
          placeholder="请输入标题..."
          v-model="biaoti"
          type="text"
          class="a8"
        />
      </div>
    </div>

    <mavon-editor
      :toolbars="toolbars"
      class="a2"
      v-model="message"
    ></mavon-editor>
  </div>
</template>
<script>
import { mavonEditor } from "mavon-editor";
import "mavon-editor/dist/css/index.css";
export default {
  components: {
    mavonEditor
  },
  name: "Home",

  data() {
    return {
      toolbars: {
        bold: true, // 粗体
        italic: true, // 斜体
        header: true, // 标题
        underline: true, // 下划线
        mark: true, // 标记
        superscript: true, // 上角标
        quote: true, // 引用
        ol: true, // 有序列表
        link: true, // 链接
        imagelink: true, // 图片链接
        help: true, // 帮助
        code: true, // code
        subfield: true, // 是否需要分栏
        fullscreen: true, // 全屏编辑
        readmodel: true, // 沉浸式阅读
        undo: true, // 上一步
        trash: true, // 清空
        save: true, // 保存（触发events中的save事件）
        navigation: true // 导航目录
      },
      message: "",
      biaoti: ""
    };
  },
  methods: {
    fabiao() {
      // var obj = { zhengwen: this.message, title: this.biaoti };
      // console.log(obj);
      // var templist = JSON.parse(localStorage.getItem("issue") || "[]");
      // templist.push(this.issue);
      // localStorage.setItem("obj", JSON.stringify(obj));
      var obj = { zhengwen: this.message, title: this.biaoti };

      var templist1 = JSON.parse(localStorage.getItem("wenzhang") || "[]");
      console.log(templist1);
      templist1.push(obj);
      console.log(templist1);
      localStorage.setItem("wenzhang", JSON.stringify(templist1));
    }
  }
};
</script>
<style scoped>
.a1 {
  height: 800px;
}
.a2 {
  width: 70%;

  height: 100%;

  box-shadow: 0 0 9px 3px #e5e2e2;
  margin: 0 auto;
  font-size: 13px;
  white-space: pre-wrap;
  font-size: 15px;
}
.wenbenkuang {
  resize: none;
  height: 100%;
  width: 90%;
  border: none;
  border-color: rgb(228, 228, 217);
  box-shadow: 0 0 9px 3px #e5e2e2;
  outline: none;
  font-size: 15px;
}
.a4 {
  width: 50%;
  height: 100%;
}
.a5 {
  width: 50%;
  height: 100%;
}
.a3 {
  display: -webkit-flex;
  flex-direction: column;
  justify-content: space-around;
}
.a6 {
  height: 20px;
  font-family: "'微软雅黑','Helvetica Neue',Helvetica,Arial,sans-serif";
  font-size: 13px !important;
  height: 30px;
  line-height: 18px !important;
  padding: 3px 18px;
  display: inline-block;
  vertical-align: middle;
  font-weight: normal;
  border-radius: 3px;
  margin: 0 8px 0 3px;
  border: none;
  color: #ffffff;
  background-color: #89bbf0;
  cursor: pointer;
  top: 50%;
}
.a7 {
  height: 60px;
}
.a9 {
  height: 75px;
}
.a8 {
  border: none;
  height: 50%;
  width: 50%;
  box-shadow: 0 0 9px 3px #e0e0e0;
  outline: none;
  font-size: 20px;
}
</style>
