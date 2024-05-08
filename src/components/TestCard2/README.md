## README

**TestCard**

此组件由 MyBricks 平台生成
地址：https://my.mybricks.world/mybricks-app-pc-cdm/index.html?id=562086822649925

**用法**

```vue
<template>
  <test-card ref="comRef" prop1="自定义值" />
</template>

<script lang="ts">
import { ref } from 'vue'
import TestCard from './TestCard.vue'

export default {
  components: {
    TestCard,
  },
  setup() {
    const comRef = ref()
    return { comRef }
  },
}
</script>
```

**注意事项**

- 组件需要在 [Vue3](https://cn.vuejs.org/) 环境中运行。
- 组件依赖的外部库需要自行安装。
- 代码中出现形似”u_0IEOE“的随机命名时，建议去MyBricks平台上补充对应的命名信息
