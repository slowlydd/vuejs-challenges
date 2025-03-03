<!--info-header-start--><h1>Effect作用域 API <img src="https://img.shields.io/badge/-%E4%B8%AD%E7%AD%89-d9901a" alt="中等"/> <img src="https://img.shields.io/badge/-%23Composition%20API-999" alt="#Composition API"/> <img src="https://img.shields.io/badge/-%23Reactivity%3AAdvanced-999" alt="#Reactivity:Advanced"/></h1><blockquote><p>By webfansplz <a href="https://github.com/webfansplz" target="_blank">@webfansplz</a></p></blockquote><p><a href="https://sfc.vuejs.org/#eyJBcHAudnVlIjoiPHNjcmlwdCBzZXR1cCBsYW5nPVwidHNcIj5cbmltcG9ydCB7IHJlZiwgY29tcHV0ZWQsIHdhdGNoLCB3YXRjaEVmZmVjdCB9IGZyb20gXCJ2dWVcIlxuXG5jb25zdCBjb3VudGVyID0gcmVmKDEpXG5jb25zdCBkb3VibGVkID0gY29tcHV0ZWQoKCkgPT4gY291bnRlci52YWx1ZSAqIDIpXG5cbi8vIHVzZSBgZWZmZWN0U2NvcGVgIEFQSSB0byBtYWtlIHRoZXNlIGVmZmVjdCBzdG9wIHRvZ2V0aGVyIGFmdGVyIHRyaWdnZXJlZCBvbmNlXG5cbndhdGNoKGRvdWJsZWQsICgpID0+IGNvbnNvbGUubG9nKGRvdWJsZWQudmFsdWUpKVxud2F0Y2hFZmZlY3QoKCkgPT4gY29uc29sZS5sb2coXCJDb3VudDogXCIsIGRvdWJsZWQudmFsdWUpKVxuXG5jb3VudGVyLnZhbHVlID0gMlxuXG5zZXRUaW1lb3V0KCgpID0+IHtcbiAgY291bnRlci52YWx1ZSA9IDRcbn0pXG5cbjwvc2NyaXB0PlxuXG48dGVtcGxhdGU+XG4gIDxkaXY+XG4gICAgPHA+XG4gICAgICB7eyBkb3VibGVkIH19XG4gICAgPC9wPlxuICA8L2Rpdj5cbjwvdGVtcGxhdGU+XG4ifQ==" target="_blank"><img src="https://img.shields.io/badge/-%E6%8E%A5%E5%8F%97%E6%8C%91%E6%88%98-213547?logo=vue.js&logoColor=42b883" alt="接受挑战"/></a> &nbsp;&nbsp;&nbsp;<a href="./README.md" target="_blank"><img src="https://img.shields.io/badge/-English-gray" alt="English"/></a> </p><!--info-header-end-->


在这个挑战中，你将使用 `响应式 API: effectScope` 来完成它。
以下是你要实现的内容 👇: 

```vue
<script setup lang="ts">
import { ref, computed, watch, watchEffect } from "vue"

const counter = ref(1)
const doubled = computed(() => counter.value * 2)

// 使用 `effectScope` API 使这些Effect效果在触发一次后停止

watch(doubled, () => console.log(doubled.value))
watchEffect(() => console.log("Count: ", doubled.value))

counter.value = 2

setTimeout(() => {
  counter.value = 4
})

</script>

<template>
  <div>
    <p>
      {{ doubled }}
    </p>
  </div>
</template>


```
<!--info-footer-start--><br><a href="../../README.zh-CN.md" target="_blank"><img src="https://img.shields.io/badge/-%E8%BF%94%E5%9B%9E%E9%A6%96%E9%A1%B5-grey" alt="返回首页"/></a> <a href="https://github.com/webfansplz/vuejs-challenges/issues/new?labels=answer,zh-CN&template=1-answer.zh-CN.md&title=8%20-%20Effect%E4%BD%9C%E7%94%A8%E5%9F%9F%20API" target="_blank"><img src="https://img.shields.io/badge/-%E5%88%86%E4%BA%AB%E4%BD%A0%E7%9A%84%E8%A7%A3%E7%AD%94-teal" alt="分享你的解答"/></a> <a href="https://github.com/webfansplz/vuejs-challenges/issues?q=label%3A8+label%3Aanswer" target="_blank"><img src="https://img.shields.io/badge/-%E6%9F%A5%E7%9C%8B%E8%A7%A3%E7%AD%94-de5a77?logo=awesome-lists&logoColor=white" alt="查看解答"/></a> <!--info-footer-end-->
