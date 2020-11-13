<template>
  <div>
    <h1 class="a1">GznnnAble'BLOG</h1>
    <div class="a6">
      <div class="home"></div>

      <div class="a2">
        <blogs
          v-for="value in items"
          :key="value.id"
          :biaoti="value.title"
          :zhengwen="value.zhengwen"
        ></blogs>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import blogs from "@/components/blogs.vue";
export default {
  name: "Home",

  components: {
    blogs
  },
  data() {
    return {
      items: JSON.parse(localStorage.getItem("wenzhang")),

      message: "",
      posts: [
        { id: 1, title: "首页" },
        { id: 2, title: "目录" },
        { id: 3, title: "联系我" }
      ],
      blogs: [
        {
          id: 1,
          biaoti: "标题一",
          zhengwen:
            "我的理解是components下的组件如helloworld.vue是级别最小的组件，可以在views下的几个组件中被引用。views下的组件是页面级的，就相当于几个页面，要先在router下导入。页面级组件的使用在App.cue"
        },
        {
          id: 2,
          biaoti: "标题一",
          zhengwen: "111"
        },
        {
          id: 3,
          biaoti: "标题一",
          zhengwen: "111"
        },
        {
          id: 4,
          biaoti: "标题一",
          zhengwen: "111"
        },
        {
          id: 4,
          biaoti: "标题一",
          zhengwen: "111"
        },
        {
          id: 4,
          biaoti: "标题一",
          zhengwen: "111"
        }
      ]
    };
  }
};
</script>
<style scoped>
.home {
  text-align: center;
  width: 60%;
  margin: 0 auto;
}
.a2 {
  display: -webkit-flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 60%;
  margin: 0 auto;
  box-shadow: 0 0 9px 3px rgb(229, 226, 226);
  height: 80%;
}
.a4 {
  width: 80%;
  color: #fff;
}
.a5 {
  width: 80%;
  color: rgb(255, 255, 255);
}
.a6 {
  display: -webkit-flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-around;
}
.a1 {
  height: 85px;
  color: #9db6d1;
}
</style>
