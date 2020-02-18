<template>
<div>
  <el-button v-for="(item,index) in [1,2]" :key="index" @click="handleClick(item)">{{item}}</el-button>
  <Page :pageNum="pageNum"/>
</div>
</template>
<script>
  import Page from '@/components/Page.vue'
  export default {
    components: {
    Page
  },
    data() {
      return {
        pageNum: 1
      };
    },
    methods: {
      handleClick(index) {
        this.pageNum= index;
      }
    }
  };
</script>