<!-- 这部分代码定义了网页的结构。它使用了Pug（之前称为Jade）模板语言，这是一种用于构建HTML的简洁语言。 -->
<template lang="pug">
//- v-app 是Vue应用的根组件，相当于整个应用的容器。  
v-app
  //- v-main 是一个Vue组件，通常用于包裹主要内容区域。
  v-main
    //- v-container 是一个Vue组件，用于创建一个容器，它限制了内容的最大宽度，使得内容在不同屏幕宽度下都能保持合理的布局。
    v-container
      //- 自定义组件  
      ui-header
      ui-hero
      ui-hairstyle
      //- ui-footer
</template>

<!-- <script setup> 是Vue 3的一个新特性，它允许我们以一种更简洁的方式编写组件的脚本。 -->
<script setup lang="ts">
// 常量，分别定义了网页的标题、描述和一张图片的URL。
const title = 'Change Hairstyle AI for FREE'
const description = 'Get a new hairstyle in seconds, for free.'
const image = 'https://changehairstyleai.com/cover.jpg'

useServerSeoMeta({
  title,
  ogTitle: title,
  description,
  ogDescription: description,
  ogType: 'website',
  ogSiteName: title,
  ogImage: image,
  twitterCard: 'summary_large_image',
  twitterTitle: title,
  twitterDescription: description,
  twitterImage: image,
  twitterCreator: 'pontusaurdal'
})
</script>

<!-- 
  组件的样式，它使用了Stylus，这是一种CSS预处理器，允许使用更高级的语法来编写样式。
  .v-application 是Vue应用的根级别的样式，这里定义了一个径向渐变背景。
  .v-container 定义了容器的最大宽度，确保内容不会在大屏幕上过宽。
 -->
<style lang="stylus" scoped>
.v-application
  background radial-gradient(80% 130% at 50% -30%, rgba(0, 0, 0, .15) 0, rgba(0, 0, 0, 0) 100%)

  .v-container
    max-width 1000px
</style>
