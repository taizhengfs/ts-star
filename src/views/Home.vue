<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld :msg="article.title" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src

export default Vue.extend({
  name: 'home',
  components: {
    HelloWorld
  },
  data () {
    return {
      article: {}
    }
  },
  created () {
    this.getArticle()
  },
  methods: {
    getArticle () {
      interface StarRules {
        title: string
        count: number
        content: string
        author: string
      }
      const article: StarRules = {
        title: '规则简介',
        count: 9999,
        content: 'xxx...',
        author: 'tzdr'
      }
      this.article = article
      enum Color {
        Red = 1,
        Green = 8,
        Blue
      }
      const yuanzu: [number, string] = [1, '2']
      console.info(yuanzu)
    }
  }
})
</script>
