# Vue 规范

*强制* `页面`或者`模块`必须采用`TypeScript`类的形式进行编写。
*强制* `页面`或者`模块`的类名必须和该`页面`或者`模块`的文件名称有关，建议完全一致。
*强制* `页面`或者`模块`必须有一个样式，并且样式名称和该`页面`或者`模块`的文件名有关，建议完全一致。
*强制* `页面`或者`模块`的 `Html`、`Less`、`Type` 必须遵循各自的代码规范。

```
// home.vue
<template>
  <div class="home">
    <banner />
    {{ message }}
    <button
      class="btn"
      @click="updateMessage()">
      click
    </button>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import Banner from './.banner.vue';

@Component({
  components: {
    Banner
  }
})
export default class Home extends Vue {
  private message: string = 'Hello World!';

  private updateMessage () {
    this.message = 'Update Message.';
  }
}
</script>

<style lang="less">
.home {
  background-color: #F8F8F8;
}
</style>

```