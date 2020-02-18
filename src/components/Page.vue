<template>
<div>
    <span>page{{change(pageShow)}}</span>
</div>
</template>
<script>
  export default {
      props: ['pageNum'],
      data(){
          return {

          }
      },
      computed: {
          pageShow(){
              return this.pageNum + '什么鬼';
          }
      },
      mounted () {
          console.log(this.pageNum)
      },
      updated () {
          console.log(this.pageNum)
      },
      destroyed () {
          console.log('destory');
      },
      methods: {
          change(pageNum){
              return pageNum + 'wtf';
          }
      }
  };
</script>