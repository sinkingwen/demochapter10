<script setup>
import ButtonCounter from "./components/ButtonCounter.vue";
//异步组件，引入defineAsyncComponent
import { defineAsyncComponent} from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import BlogPost from "@/components/BlogPost.vue";
import ParentComp from "@/components/ParentComp.vue";
import CardComponent from "./components/CardComponent.vue";
import ModelView from '@/components/ModelView.vue'
import { ref } from "vue";
// 异步组件
// const ButtonCounter = defineAsyncComponent(() =>
//   import("@/components/ButtonCounter.vue")
// );

const posts = ref([
  { id: 1, title: "My journey with Vue" },
  { id: 2, title: "Blogging with Vue" },
  { id: 3, title: "Why Vue is so fun" },
]);
const postFontSize = ref(1);
</script>

<template>
  <div>
    <HelloWorld msg="HelloWorld"></HelloWorld>
    <ButtonCounter></ButtonCounter>
    <div :style="{ fontSize: postFontSize + 'em' }">
      <blog-post
        v-for="post in posts"
        :title="post.title"
        :key="post.id"
        @enlarge-text="postFontSize += 0.1"
        @update-title="post.title = 'Vue3'"
      ></blog-post>
    </div>
    <ParentComp></ParentComp>
    <div class="slotbox">
      <!-- <CardComponent>卡片组件</CardComponent> -->
      <CardComponent>
        <template #header><h2>卡片头部</h2></template>
        <template v-slot:footer><h4>卡片结尾</h4></template>
      </CardComponent>
    </div>
    <div class="custom-model">
      <model-view></model-view>
    </div>
  </div>
</template>
<style scoped>
.slotbox {
  margin-top: 30px;
  background-color: #e4e4e4;
}
.custom-model{
  height: 80px;
  margin-top:30px ;
  background-color: rgb(146, 202, 146);
}
</style>
