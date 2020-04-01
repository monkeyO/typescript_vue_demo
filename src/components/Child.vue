<template>
  <div class="hello">
    <h1>项目名：{{cName}}</h1>
    <h2 ref="age">版本：{{cAge}}</h2>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component({ name: "Child" })
export default class Child extends Vue {
     cName: string = "子元素名";
     cAge: string = "v1.0.1";
   makeDetail(){
    const refs:any = this.$refs.age;
    console.log("当前节点：：",refs.innerHTML);
  }

  mounted() {
     
  }
}
</script>